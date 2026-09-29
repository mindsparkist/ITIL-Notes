Here’s a realistic composite story — not an official Subway event, but the kind of thing that happens in real IT. Use it as your memory hook.

## The Monday Lunch Rush Meltdown

It’s Monday, 11:42 AM. Lunch rush is starting.

At about 1,200 Subway stores across the Midwest, the POS terminals suddenly show:

> “Payment gateway unreachable.”

Stores can’t take card payments. The Subway app and third-party delivery orders start failing. Some stores switch to cash only. Franchisees are calling. Store managers are calling. Your phone is blowing up.

You’re the Major Incident Manager. You declare a **Major Incident** — SEV1/P1.

You open the bridge and get the right people on:
- POS support
- Network team
- Payment gateway vendor
- Store operations
- Cloud/infrastructure
- Change manager

Your job as MIM is not to fix it yourself. Your job is to:
- Restore service as fast as possible
- Coordinate the technical teams
- Communicate to the business
- Keep a timeline
- Make sure a workaround happens
- Hand off to Problem Management afterward

At 11:55 AM, someone says:

> “We pushed a firewall rule change at 10:15 AM to block an old vulnerable port. It may have accidentally blocked the payment gateway port too.”

Now you have a suspected cause.

You ask:

> “Can we roll it back?”

Network says:

> “We can, but it reopens the security hole.”

You ask the Change Manager:

> “Can we do an emergency change to add an exception for the payment gateway IPs?”

Change Manager says:

> “Yes. Emergency change approved verbally. Do it now, document it after.”

At 12:20 PM, network adds the exception. At 12:35 PM, card payments start working again. You close the Major Incident.

Lunch rush is saved — mostly.

## Now the Problem Management part

The incident is over, but the cause is not fixed.

A **Problem Manager** raises a Problem record:  
**PRB-001: Card payment failures after firewall rule change.**

Problem Management asks:
- Why did the firewall rule block the payment gateway?
- Why didn’t testing catch it?
- Why didn’t the change record show the payment gateway dependency?
- Was this a one-off or could it happen again?

They find the root cause:
- The firewall rule was meant to block port 445.
- Due to a rule-order mistake, it also blocked port 8443 to the payment gateway.
- The test stores used a different payment route, so tests passed.
- The CMDB did not show the payment gateway dependency.
- The change was rolled out to all stores at once instead of gradually.

Outputs of Problem Management:
- **Root cause:** mis-scoped firewall rule.
- **Known Error:** “Firewall rule FW-2024-XX blocks payment gateway port 8443.”
- **Workaround:** reroute to backup payment gateway, or cash-only.
- **Permanent fix needed:** correct the firewall rule and improve testing/rollout.

## Now the Change Management part

Problem Management says: “We need a permanent fix.”

That permanent fix is a **Change**.

A Change Request is raised:  
**CHG-0456: Correct firewall rule and add canary rollout for store network changes.**

Change Management asks:
- What exactly will change?
- What is the risk?
- What is the backout plan if it breaks?
- Who tested it?
- What is the impact?
- When should we do it?
- Does CAB approve it?

They decide:
- Fix the firewall rule.
- Add the payment gateway to the approved exception list.
- Roll out to 1% of stores first.
- Run an automated test transaction.
- Wait 24 hours.
- Then roll out to the rest.
- Schedule it for Tuesday at 2:00 AM, low traffic.
- Have a rollback plan ready.

CAB approves it. The change is implemented successfully. Post-Implementation Review confirms no issues. The Known Error is closed.

## The simple memory version

| Process | Question it answers | Subway example |
|---|---|---|
| Incident Management | What is broken right now? | Card payments failing at 1,200 stores |
| Major Incident Management | How do we restore service fast? | Bridge, comms, workaround, emergency change |
| Problem Management | Why did it break, and how do we stop it repeating? | Firewall rule blocked payment gateway |
| Change Management | How do we put the permanent fix in safely? | CAB-approved firewall fix with canary rollout |

## Remember it like this

- **Incident** = “The store is on fire.”
- **Problem** = “Why did it catch fire? Faulty wiring.”
- **Change** = “How do we replace the wiring across all stores without burning down another one?”

As a former MIM, you lived mostly in the first box. But you touched the other two at the edges:
- You raised the Problem record after the Major Incident.
- You invoked an Emergency Change for the workaround.
- You joined the Post-Incident Review.
- You helped the Problem Manager with your timeline.
- You helped Change Management understand what went wrong.

If you remember nothing else:

> **Incident restores service. Problem finds the cause. Change fixes it permanently without causing the next incident.**
