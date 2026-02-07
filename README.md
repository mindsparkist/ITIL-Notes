Transitioning into a **Major Incident Management (MIM)** role is all about moving from a "fixer" mindset to an "orchestrator" mindset. As an entry-level MIM, your goal isn't to log into the servers yourself; it’s to command the room, manage the clock, and protect the business.

Here is a structured guide designed for a high-impact MIM documentation.

---

## 1. Defining a Major Incident (MI)

Not every outage is a Major Incident. An MI is defined by **Urgency** and **Impact**.

* **Impact:** The measure of the effect on business processes (e.g., "5,000 users cannot process payments").
* **Urgency:** How quickly the business needs a resolution (e.g., "The payment gateway is down during a flash sale").

---

## 2. The MIM Lifecycle

A Major Incident follows a strict, repeatable path. Your job is to drive the incident through these stages:

1. **Identification & Validation:** Confirming the issue is truly an MI.
2. **Notification:** Sending the initial "Heads up" to stakeholders.
3. **Mobilization:** Getting the right technical experts on a bridge (Zoom/Teams/Phone).
4. **Mitigation:** Finding a "Workaround" to restore service quickly, even if the root cause isn't fixed yet.
5. **Resolution:** The permanent fix is applied.
6. **Post-Incident Review (PIR):** Discussing what went wrong to prevent it from happening again.

---

## 3. Communication Standards

In MIM, **Communication is Currency.** If you aren’t communicating, people assume nothing is happening.

### Internal Technical Bridge (The "War Room")

* **Keep it focused:** Don't let engineers "rabbit hole" into minor details.
* **The 15-Minute Rule:** Ask for a status update every 15–20 minutes.
* **Scribe:** If you don't have a dedicated scribe, you must document every major action taken in the ticket.

### External Stakeholder Updates

Use the **"What, Who, When"** format:

* **What** is happening? (Current Status)
* **Who** is affected? (Scope)
* **When** is the next update? (ETA for next comms)

---

## 4. Key Rituals: The Bridge Kick-off

When you start a bridge, you set the tone. Use this script:

> "This is [Name], the Major Incident Manager. We are here for MI #[Number] regarding [Service]. The current impact is [X]. [Lead Engineer], please give us a 30-second summary of what we know and what the current action plan is."

---

## 5. The Post-Incident Review (PIR)

The PIR is where the real value is created for the company. You are looking for the **Root Cause**.

| Question to Ask | Why it matters |
| --- | --- |
| **Why did this happen?** | To find the technical root cause. |
| **Why did we not catch it sooner?** | To improve monitoring and alerting. |
| **How can we automate the fix?** | To reduce future "Mean Time to Repair" (MTTR). |

---

### Pro-Tips for the Entry-Level MIM:

* **Stay Calm:** If the MIM panics, everyone panics. Your voice should be the "steady hand."
* **Don't Fear Silence:** Sometimes engineers need 5 minutes of silence to actually think. Give them space, then pull them back.
* **Focus on the Clock:** Always be aware of Service Level Agreements (SLAs). If you are 30 minutes away from a breach, escalate to management immediately.

Would you like me to draft a **standardized email template** for your first "Major Incident Initial Notification"?




Here is a clean, professional template for an **Initial Major Incident Notification**.

As an entry-level MIM, remember that the goal of this first email is to stop the influx of "is it down?" queries by proving that the Incident Management team is already on top of it.

---

## **Major Incident Initial Notification**

**Subject:** INITIAL NOTIFICATION: [Priority] | [Service Name] | [Brief Description of Issue]

**Body:**

> **Incident Reference:** MI-[12345]
> **Priority:** P1 - Critical
> **Service Affected:** [e.g., Global Payment Gateway / Internal ERP]
> ---
> 
> 
> **Current Status:** > We have identified a significant disruption affecting [Service Name]. Technical teams have been mobilized, and a restoration bridge is currently active.
> **Business Impact:** > Users are currently unable to [e.g., process transactions / log into the portal]. This is affecting [all users / users in the APAC region].
> **Action Taken:** > * Technical Bridge opened at [Time + Timezone].
> * Server logs are being reviewed for potential database latency.
> * Networking teams are investigating recent firewall changes.
> 
> 
> **Next Update:** > An update will be provided in **30 minutes** (by [Insert Time]) or sooner if significant progress is made.
> ---
> 
> 
> **Major Incident Manager:** [Your Name]
> **Bridge Link/Details:** [Insert Link if applicable for stakeholders]

---

### **3 Golden Rules for this Template:**

1. **Be Jargon-Free:** Stakeholders (Managers, Directors) read this. Instead of saying "We are seeing 503 errors on the load balancer," say "The login page is currently unavailable."
2. **The "Next Update" Promise:** This is the most important part. If you say you’ll update in 30 minutes, **send something** in 30 minutes—even if it's just to say "Investigation is still ongoing."
3. **Use "Red-Amber-Green" Logic:** If your email tool supports it, use a small red banner at the top so it's instantly recognizable as a critical alert in a crowded inbox.

ITIL is a best-practice framework designed to align IT services with business objectives and strategy.

The ITIL Service Lifecycle

Service Strategy: Aligning IT capabilities with business goals.

Service Design: Architecting services and processes to meet business needs.

Service Transition: Managing change and risk during deployment.

Service Operation: Ensuring stable, day-to-day service delivery (where MIM lives).

Continual Service Improvement (CSI): Iterative refinement of services and efficiency.

Service Operation: Ensuring stable, day-to-day service delivery (where MIM lives). -> 

In Service Operation, the primary goal is "Business as Usual" (BAU). While other functions focus on the future, Service Operation focuses on the now.

As an entry-level MIM, you are the "Emergency Room Doctor" of this stage. When the stable environment breaks, you step in to restore order.

1. How the MIM is Involved in Service Operation
The MIM role is the most critical "reactive" function in this phase. Your involvement is triggered by a Priority 1 (P1) or Priority 2 (P2) incident.

Restoration over Repair: Your job isn't to find out why a server crashed (Root Cause), but to get the business running again immediately (Workaround).

Command & Control: You lead the technical teams. You decide when to "pull the trigger" on a failover or a system reboot.

Stakeholder Shield: You handle the "What's going on?" emails from executives so the engineers can focus on fixing the code.

Escalation Path: You determine if an incident is getting worse and requires "Hierarchical Escalation" (calling the VPs or Directors).

The primary objective of Major Incident Management is to minimize business downtime and mitigate service degradation, ensuring the rapid restoration of normal service operations."
and educe Mean Time to Repair (MTTR).

Defining an Incident
An Incident is any unplanned interruption to an IT service or a reduction in the quality of an IT service.

Key Characteristics:
Unplanned: If it’s a scheduled maintenance, it’s not an incident.

Disruptive: It stops a user from working or prevents a system from performing its intended function.

Failure-based: Something that should be working has failed (e.g., "The printer is jammed" vs. "I need a new printer").

Incident vs. Service Request
A common mistake for newcomers is confusing these two. Here is how to tell them apart:

Feature,Incident,Service Request
Nature,Something is broken.,Something is needed.
Example,"""I cannot log into my email.""","""I need access to a new mailbox."""
Goal,Restore service ASAP.,Fulfill the user's request.
Urgency,Usually high.,Usually low/standard.

The "Incident" vs. "Major Incident" Distinction
Since you are training for MIM, your documentation should clarify that while all Major Incidents are incidents, not all incidents are Major Incidents.

Incident: Affects one user or a small group (e.g., a single laptop crash). Managed by the Service Desk.

Major Incident: Affects a critical business service or a large number of users (e.g., the entire company's email is down). Managed by you.

MIM Mantra: An incident is a "problem for a person." A Major Incident is a "problem for the business."

Frame this by distinguishing between the symptom (Incident) and the source (Problem).
A Problem is the underlying cause of one or more Incidents. While Incident Management focuses on restoration, Problem Management focuses on identifying and eliminating the root cause to prevent recurrence.

Problem Management is triggered when an incident recurs or remains unresolved, necessitating a Root Cause Analysis (RCA) to prevent future service disruptions.

Key Professional Concepts to Include:
Trend Analysis: This is the act of looking at "multiple times" an incident happens to find a pattern.

Reactive vs. Proactive:

Reactive Problem Management: Responding to a Major Incident that just happened.

Proactive Problem Management: Finding and fixing a problem before it causes an incident.

KEDB (Known Error Database): This is where Problem Management stores the "Root Cause" and "Workaround" so you, as the MIM, can find it quickly next time.

Why this is vital for an MIM:
If you are managing the same Major Incident for the third time in a month, the business will ask why. Your documentation should state that "MIM is responsible for restoring service, while Problem Management is responsible for ensuring the incident never returns.

Change Management is the process of authorizing and coordinating the addition, modification, or removal of any Configuration Item (CI) or service component. Its primary goal is to implement improvements while minimizing risk to the live environment.

Following Problem Management, Change Management governs updates to the Configuration Management Database (CMDB). It ensures that every alteration to resources—whether adding, deleting, or modifying—is documented and risk-assessed.

The "Big Three" Connection
For an entry-level MIM, understanding how these three interact is your "North Star":

Incident Management (MIM): "The house is on fire! Put it out now (Workaround)."

Problem Management: "Why did the house catch fire? (Root Cause)."

Change Management: "Let’s rewire the house so it doesn't happen again (Controlled Implementation)."

Key Terminology for your Documentation:
CI (Configuration Item): Any component that needs to be managed to deliver an IT Service (Server, Software, Documentation, etc.).

CMDB (Configuration Management Database): The central "map" of all your CIs and how they connect.

Standard vs. Normal vs. Emergency Change: * Emergency Change: This is what you, as an MIM, will deal with most. It’s a change that must be implemented immediately to resolve a Major Incident.

Emergency Change Request (ECR) Template
Subject: EMERGENCY CHANGE: [Incident #] | [Brief Description of Change]

1. Change Overview

Associated Major Incident: MI-[Number]

Requested By: [Lead Engineer Name / Team]

Change Description: (e.g., "Rebooting Database Cluster B to clear hung sessions.")

2. Justification

Why now? (e.g., "Service is currently 100% unavailable; standard troubleshooting has failed to restore connectivity.")

3. Impact & Risk

Service Impact: [e.g., Temporary 2-minute disconnect for remaining active sessions]

Risk Level: [High/Medium/Low]

4. Implementation Plan

Step 1: Drain traffic from Node B.

Step 2: Execute restart command.

Step 3: Validate health check URL.

5. Back-out Plan (Crucial!)

Rollback Steps: If the restart fails, we will revert to the previous configuration snapshot taken at [Time].

MIM & The Change Management Lifecycle
In an entry-level role, you must understand that even in an emergency, we don't just "change things" without a record.

The ECAB (Emergency Change Advisory Board)
When a Major Incident is occurring, you cannot wait for the weekly Change Board meeting. Instead, you convene an ECAB.

Who is in it? Usually you (the MIM), the Technical Lead, and a Service Owner/Director.

Your Role: You facilitate the "Go/No-Go" decision. You ask: "Do we have a back-out plan if this makes things worse?"

Updating the CMDB
Once the change is successful, the Configuration Management Database (CMDB) must be updated.

Configuration Item (CI): This is the specific asset you changed (e.g., a specific Linux Server or a Router).

The Result: By updating the CI, you ensure the next person who looks at that server knows exactly what was modified and why.

Incidnet comes via applicable channels (Call/Email/Chats) -> Case is logged (Service Request/Incident) -> IF Incident -> IF Qualify for MIM? -> (MIM Team) -> (Functional/hierarchical Escalation) -> MIM Brigde -> Restore the service -> Restoration + Confirmatoin of resolution form Customer =  Resolve the issue, 

IF needs monitoring create child ticket -> and put to concerned team. 

MIM is Bridge between Technical VS Management people, 

ButterFly Effect -> One change here will do an impact there 

The Attached Image for butterfly investigatoin 

------------------------------------------------------------------------------------------------------
The Professional version of above is written here
-----------------------------------------------------------------------
This is a fantastic high-level view of the MIM lifecycle. To make this professional for your documentation, we should refine the "Butterfly Effect" concept into **Impact Analysis** and polish the workflow into a "Standard Operating Procedure" (SOP).

---

## **Major Incident Management (MIM) Workflow SOP**

### **1. Entry & Classification**

Incidents are ingested via omnichannel sources (**Phone, Email, Chat, or Automated Monitoring**).

* **Initial Triage:** Categorize as a **Service Request** (User Need) or **Incident** (Service Failure).
* **MIM Qualification:** If the incident meets the pre-defined **Urgency & Impact** criteria, it is escalated to the MIM Team.

### **2. Escalation & Command**

* **Functional Escalation:** Engaging the technical SMEs (Subject Matter Experts) required to fix the issue.
* **Hierarchical Escalation:** Notifying leadership/management regarding business risk and SLA status.
* **The MIM Bridge:** The MIM acts as the **strategic interface**, translating technical jargon into business status updates for management.

### **3. Restoration & Validation**

* **Primary Objective:** Restore "Normal Service Operation" immediately.
* **Resolution Confirmation:** Service is only considered "Resolved" once the technical fix is applied **and** the business/customer confirms restoration.

### **4. Post-Restoration Governance**

* **Active Monitoring:** If the service requires post-fix observation, create a **Child Ticket** and assign it to the relevant functional team for stability monitoring.
* **Butterfly Effect (Dependency Mapping):** Every change within the IT ecosystem carries the risk of unforeseen downstream impacts. MIMs must utilize the **CMDB** to perform a "Butterfly Investigation"—analyzing how a fix in one area might trigger an outage in another.

---

## **The MIM Strategic Role: "The Bridge"**

As an MIM, you sit at the center of two critical groups:

* **Technical Teams:** Focused on logs, code, and infrastructure.
* **Management:** Focused on revenue, reputation, and customer experience.
* **Your Value:** You filter the technical noise to provide management with a clear, actionable business narrative.

---

### **Key Professional Terms Used:**

* **Omnichannel Ingestion:** Professional way to say "Call/Email/Chat."
* **SOP (Standard Operating Procedure):** The professional term for a workflow.
* **Dependency Mapping:** The technical term for your "Butterfly Effect."
* **SME (Subject Matter Expert):** The engineers on your bridge.

### **Next Step:**

This image provides an excellent visual framework for **Functional and Hierarchical Escalation**. It breaks down the chaotic "Major Incident" into a structured wing-based investigation.

Here is the professional breakdown of the steps as illustrated in your **Butterfly Investigation** model:

---

## **The Butterfly Investigation: Escalation & Resolution Steps**

### **Phase 1: Pre-Escalation (The Antennae)**

Before the bridge is fully mobilized, the MIM must define the scope of the "flight":

* **Issue Identification:** Clearly define the problem statement—what is actually broken?
* **Impact Assessment:** Determine the severity (P1/P2) and identify which business services are down.
* **Team Identification:** Pinpoint exactly which technical teams (Database, Network, Cloud) are required for the bridge.

---

### **Phase 2: Initial Investigation (The Upper Wings)**

Once the "Escalation" spine is active and teams are on-call:

* **SME Activation:** Engage Subject Matter Experts (SMEs) to perform an immediate deep-dive.
* **Initial Findings:** Gather the first set of diagnostic data to understand the "Why" behind the failure.

---

### **Phase 3: Troubleshooting & Strategic Planning (The Lower Wings)**

This is where the MIM drives the "Plan of Action":

* **Collaborative Planning:** Work with SMEs, SDEs (Software Development Engineers), and QA to validate potential fixes.
* **Parallel Pathing (Plan A & Plan B):** Always maintain a primary restoration plan (Plan A) and a contingency/rollback plan (Plan B) to mitigate the "Butterfly Effect" of a failed fix.
* **Time Management:** Set strict "Reconvene" times to validate progress and move closer to service restoration.

---

### **Phase 4: Closure & Documentation (The Base)**

The incident isn't over until the documentation is as solid as the fix:

* **The "Why, How, What" Summary:** Summarize the root cause, the resolution steps taken, and the specific plan executed.
* **Lifecycle Handover:** Determine if the incident requires a transition into **Problem Management** or **Change Management** for a permanent architectural fix.

---

### **Professional Summary for your Documentation:**

> "The Butterfly Investigation model ensures that escalation is not just a call for help, but a structured expansion of technical expertise. By balancing initial investigation with dual-path planning (Plan A/B), the MIM maintains control over the incident lifecycle from identification to validated closure."


the **"Butterfly Investigation"** image, 

![Butterfly Investigation Diagram](https://raw.githubusercontent.com/mindsparkist/ITIL-Notes/refs/heads/main/Butterfly.png)


This **MIM One-Page Playbook** is designed to be your "cheat sheet" during high-pressure outages. It condenses the ITIL framework into actionable steps for an entry-level manager.

---

# Major Incident Management (MIM) Playbook

## 1. The Core Philosophy

**Goal:** Restore service as fast as possible.
**Mantra:** "Restoration over Repair." We find a workaround now; Problem Management finds the root cause later.

---

## 2. The Service Lifecycle Connection

* **Service Operation:** This is your home. You ensure daily stability.
* **Incident:** A service disruption.
* **Major Incident (MI):** A high-impact disruption affecting critical business functions.
* **Problem:** The underlying root cause (investigated post-MI).
* **Change:** The authorized modification of a **Configuration Item (CI)** in the **CMDB** to apply a fix.

---

## 3. Incident Priority Matrix

| Impact \ Urgency | High (Critical Business) | Medium (Team/Dept) | Low (Individual) |
| --- | --- | --- | --- |
| **High** | **P1 - Major Incident** | P2 - High | P3 - Moderate |
| **Medium** | P2 - High | P3 - Moderate | P4 - Low |

---

## 4. The Execution Workflow

1. **Validate:** Confirm the impact. Is it truly a P1?
2. **Mobilize:** Open the technical bridge. Record the start time.
3. **Notify:** Send the "Initial Notification" to stakeholders within 15 mins.
4. **Orchestrate:** * Ask for updates every 15-20 mins.
* Prevent "rabbit-holing."
* Ask: *"Is there a workaround we can apply immediately?"*


5. **Emergency Change (ECR):** If a fix is found, ensure a **Back-out Plan** exists before implementation.
6. **Resolve:** Confirm with the business that service is restored.
7. **Handover:** Transfer the incident details to **Problem Management** for Root Cause Analysis (RCA).

---

## 5. Communications Checklist

* **Initial:** Sent? Yes/No
* **Status Updates:** Sent every 30-60 mins? Yes/No
* **Resolution:** Sent with impact duration and workaround details? Yes/No

---

## 6. Pro-Tips for the Entry-Level MIM

* **The Scribe Rule:** Document everything (Time, Action, Owner) in the ticket. If it isn't in the ticket, it didn't happen.
* **Control the Bridge:** If the call gets chaotic, mute everyone and reset the agenda. You are the conductor of the orchestra.
* **The CMDB Check:** When a fix is proposed, ask: *"Which CI are we touching, and what else is connected to it?"*

---
A **Post-Incident Review (PIR)** is the most important document you will produce after the "fire" is out. It demonstrates your value as a Business Solutions Analyst by translating technical chaos into business intelligence.

Here is a professional template.

---

## **Major Incident Report / PIR Template**

### **1. Executive Summary**

* **Incident Reference:** MI-[Number]
* **Service Impacted:** [e.g., Client Facing Portal / SAP Environment]
* **Total Downtime:** [X] hours, [Y] minutes
* **Severity:** P1 - Critical
* **Summary:** A brief 2-sentence overview of what happened and how it was fixed.

### **2. Incident Timeline (The "Pulse")**

| Time (IST) | Action / Event | Owner |
| --- | --- | --- |
| **14:00** | Monitoring Alert triggered for Database Latency. | Event Mgmt |
| **14:15** | Major Incident Declared; Bridge opened. | MIM |
| **14:45** | Root Cause identified as a failed storage controller. | Infrastructure |
| **15:10** | **Emergency Change (ECR)** approved to failover to DR. | ECAB |
| **15:45** | Service Restored via Disaster Recovery site. | Tech Lead |

### **3. Root Cause Analysis (RCA)**

* **Primary Cause:** What actually broke? (e.g., Hardware failure, Code bug, Human error).
* **Contributing Factors:** Was there a delay in notification? Did a secondary tool fail?
* **Trigger:** What was the specific event that started the outage?

### **4. Resolution & Workaround**

* **Short-term Fix:** Describe the workaround used to restore service.
* **Long-term Fix:** What needs to be changed in the **CMDB** or infrastructure to prevent this from happening again?

### **5. Lessons Learned & Action Items**

| Action Item | Owner | Target Date |
| --- | --- | --- |
| Update monitoring thresholds for storage alerts. | Cloud Team | Feb 20, 2026 |
| Review failover documentation for accuracy. | Documentation | Feb 25, 2026 |
| Conduct a Problem Management deep-dive on vendor hardware. | Problem Mgmt | Mar 01, 2026 |

---

## **Professional Advice for the PIR Meeting**

As the MIM, you will likely facilitate the meeting where this report is discussed. Keep these tips in mind:

* **No Blame Culture:** The goal is to fix the *process*, not to punish the *person* who made a mistake.
* **Data is King:** Since you’re a Business Solutions Analyst, use metrics. Mention the **SLA (Service Level Agreement)**—did you stay within the allowed downtime limits?
* **The "Five Whys":** Always ask "Why" five times to get past the symptom and find the real problem.

---

### **Finalizing your MIM Documentation**

You now have a complete toolkit:

1. **Playbook** for live incidents.
2. **Notification Templates** for communication.
3. **Emergency Change** procedures for the CMDB.
4. **PIR Template** for post-incident reporting.

Using Generative AI to automate your **Post-Incident Review (PIR)** is a game-changer for an MIM. Instead of spending hours scrolling through Slack logs or Zoom transcripts, you can use a Large Language Model (LLM) to extract the timeline and key decisions instantly.

---

## 1. The "Master Prompt" for PIR Generation

Copy and paste this prompt into an LLM (like Gemini) along with your raw incident chat logs or transcript.

> **Prompt:**
> "You are an expert Major Incident Manager. Below is a raw transcript from a technical bridge. Please transform this into a structured **Post-Incident Review (PIR)** report.
> **Requirements:**
> 1. **Executive Summary:** A high-level 2-sentence summary of the impact and resolution.
> 2. **Timeline:** Create a chronological table of key events (Detection, Mobilization, Investigation, Change Implementation, Restoration).
> 3. **Root Cause:** Identify the primary technical failure mentioned.
> 4. **Action Items:** Extract any follow-up tasks mentioned by engineers.
> 5. **Tone:** Professional, objective, and business-focused.
> 
> 
> **Transcript:**
> [Paste your Slack logs or Zoom transcript here]"

---

## 2. GenAI Tools for MIM

If you want to move beyond simple prompts and automate this at scale, consider these industry-standard tools that many firms use:

* **ServiceNow (Now Assist):** Automatically summarizes incidents and generates PIR drafts directly within the ticket.
* **PagerDuty (Advance):** Uses AI to "wrap up" Slack conversations into a concise summary once an incident is resolved.
* **Datadog Incident AI:** Automatically detects related incidents and suggests follow-up tasks based on chat history.
* **n8n / Zapier:** You can build a custom workflow that takes a resolved Jira ticket, sends the description to an LLM, and emails you a drafted PIR.

---

## 3. The "Human-in-the-Loop" Rule

As an entry-level MIM, **never** send an AI-generated PIR directly to stakeholders without reviewing it. AI can sometimes "hallucinate" (make up) technical details or miss the nuance of a business impact.

**Your Review Checklist:**

* **Timestamps:** Are the times accurate? (AI sometimes struggles with different time zones).
* **CIs (Configuration Items):** Did it identify the correct server or database from the CMDB?
* **Accountability:** Ensure the PIR doesn't sound like it's "blaming" a specific person; keep it focused on the system failure.

---





