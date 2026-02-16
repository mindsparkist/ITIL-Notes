## **1. What is Change Management?**

Change Management is the process of authorizing and coordinating any addition, modification, or removal of a **Configuration Item (CI)** or IT service.

* **Goal:** To implement beneficial changes with minimum disruption to IT services.
* **The MIM Connection:** Most Major Incidents are actually caused by a "bad change" (a patch or update that wasn't tested). Conversely, most Major Incidents are resolved by an "Emergency Change."

---

## **2. The Three Types of Changes**

As an MIM, you need to know which "lane" your technical team is driving in:

| Change Type | Description | Risk Level | MIM Involvement |
| --- | --- | --- | --- |
| **Standard** | Low-risk, pre-authorized, and repetitive (e.g., password reset). | Low | None. |
| **Normal** | Requires a formal review by the **Change Advisory Board (CAB)**. Follows a scheduled timeline. | Medium/High | Low (usually informed). |
| **Emergency** | A change that must be implemented **immediately** to resolve a Major Incident. | Very High | **High (You drive this).** |

---

## **3. The Change Management Lifecycle (For MIMs)**

When a fix is found during your bridge, it follows this simplified path:

1. **Request for Change (RFC):** The engineer proposes the fix.
2. **Assessment:** You and the technical lead evaluate the **impact** and **risk**.
3. **Authorization (ECAB):** You convene the **Emergency Change Advisory Board** (usually you, the Service Owner, and a Director) for a quick "Go/No-Go" decision.
4. **Implementation:** The fix is applied to the live environment.
5. **Review:** Was the change successful? If not, you trigger the **Back-out Plan**.
6. **CMDB Update:** The **Configuration Management Database** is updated to reflect the new state of the infrastructure.

---

### **Professional Summary for your Documentation:**

> "Change Management provides the governance and risk-assessment framework required to implement fixes. For an MIM, it is the mechanism used to transform a 'Workaround' into a 'Permanent Resolution' while safeguarding the stability of the CMDB."

When you are on a high-pressure Major Incident bridge, you don't have time for long debates. You need a structured, professional way to get an **Emergency Change** authorized so you can restore service.

Use this script to transition from **Incident Management** to **Change Governance** seamlessly.

---

## **The Emergency Change (ECR) Authorization Script**

### **Step 1: The Briefing (To the Technical Team)**

> "Team, we have identified the proposed fix: [Describe fix, e.g., Failing over to the DR site]. Before we proceed, I need to confirm: What is the estimated downtime during the change, and do we have a validated **Back-out Plan** if this fails?"

### **Step 2: The Pitch (To the Change Approver/Director)**

> "[Name], we are seeking approval for an **Emergency Change** to resolve MI-[Number].
> * **The Plan:** [Briefly describe the action].
> * **Risk:** The risk is [Low/Medium/High] because [Reason].
> * **Impact:** This will restore service for [X] users.
> * **Safety Net:** If unsuccessful, we can roll back to the current state within [X] minutes.
> Do I have your authorization to proceed?"
> 
> 

### **Step 3: The Record (Post-Approval)**

> "Authorization received at [Time]. [Lead Engineer], you are clear to implement. I am noting this approval in the incident log and will update the **CMDB** accordingly."

---

## **How Change Management Protects the MIM**

| Feature | How it helps the Entry-Level MIM |
| --- | --- |
| **Peer Review** | Ensures a second pair of eyes looks at the code/fix before it hits production. |
| **Risk Mitigation** | Forces the team to think about the "Butterfly Effect" before they act. |
| **Audit Trail** | Provides a legal and professional record of who authorized the fix and why. |
| **Conflict Detection** | Checks if another team is doing a different change at the same time that might clash. |

---

## **The MIM "Golden Question" for Change**

Before any button is pushed, always ask:

> **"Which Configuration Item (CI) are we modifying, and what are its upstream dependencies?"**

This question proves you are thinking like a **Business Analyst**. It shows you aren't just looking at a server; you are looking at the entire business service map.

---
In Change Management, the **7 Rs** serve as a critical checklist for the Change Advisory Board (CAB) and the MIM to evaluate the risk and necessity of a proposed fix. This framework ensures that no "Butterfly Effect" is overlooked before a change is authorized.

---

## **The 7 Rs of Change Management**

### **1. Who RAISED the change?**

* **The Goal:** Identify the stakeholder or system that initiated the request.
* **MIM Context:** Knowing if a change was raised by a Senior Engineer or an automated monitoring tool helps determine the initial level of technical trust.

### **2. What is the REASON for the change?**

* **The Goal:** Understand the "Why." Is it to fix a Major Incident, or is it a routine update?
* **MIM Context:** In an emergency, the reason is always **Service Restoration**.

### **3. What is the RETURN required?**

* **The Goal:** Define the expected outcome or business benefit.
* **MIM Context:** The "Return" is the elimination of downtime and the return to "Normal Service Operation."

### **4. What are the RISKS involved?**

* **The Goal:** Identify potential failures or the "Butterfly Effect."
* **MIM Context:** This is the most important "R." You must ask: *"If we apply this patch, what is the worst-case scenario?"*

### **5. What RESOURCES are required?**

* **The Goal:** Determine the people, tools, and time needed to implement the change.
* **MIM Context:** Do we have the right SMEs on the bridge to execute this fix right now?

### **6. Who is RESPONSIBLE for the build and implementation?**

* **The Goal:** Assign clear accountability.
* **MIM Context:** In your incident log, you must document exactly who is "pressing the button" and who is validating the result.

### **7. What is the RELATIONSHIP with other changes?**

* **The Goal:** Check for dependencies and conflicts in the CMDB.
* **MIM Context:** Are there other teams performing maintenance that might conflict with our emergency fix?

---

### **Applying the 7 Rs on an Emergency Bridge**

As an entry-level MIM, you don't need to write a long essay for each "R." Instead, use them as a **rapid-fire mental checklist** before you give the "Go" signal:

> *"Team, we know who **Raised** this and the **Reason**. We know the **Return** is service restoration. Now, let's talk **Risk**: what are the **Relationships** with other CIs, do we have the **Resources** on the line, and who is **Responsible** for the back-out plan?"*

---
While ITIL v3/2011 originally defined **26 processes** organized into 5 lifecycle stages, it is important for an entry-level MIM to know that ITIL 4 has evolved these into **34 Practices**.

However, to master your documentation and pass standard certifications, understanding the classic 26-process map is essential. Here is the crisp, professional breakdown:

---

## **The 26 Processes of ITIL (by Lifecycle Stage)**

### **1. Service Strategy (5 Processes)**

*Focus: Defining the market, business goals, and financial viability.*

1. **Strategy Management for IT Services:** Developing the service provider's strategy.
2. **Service Portfolio Management:** Managing the entire suite of services.
3. **Financial Management for IT Services:** Managing budgeting and accounting.
4. **Demand Management:** Understanding and influencing customer demand.
5. **Business Relationship Management (BRM):** Maintaining positive links with customers.

### **2. Service Design (8 Processes)**

*Focus: Designing the service, architecture, and governance.*
6.  **Design Coordination:** Ensuring consistent design across all projects.
7.  **Service Level Management (SLM):** Negotiating SLAs and ensuring they are met.
8.  **Service Catalogue Management:** Ensuring an accurate list of live services is available.
9.  **Availability Management:** Ensuring services meet agreed availability needs.
10. **Capacity Management:** Ensuring IT resources meet performance/throughput targets.
11. **IT Service Continuity Management (ITSCM):** Managing disaster recovery and business continuity.
12. **Information Security Management:** Protecting data, assets, and services.
13. **Supplier Management:** Managing third-party vendors and contracts.

### **3. Service Transition (7 Processes)**

*Focus: Building, testing, and deploying services.*
14. **Transition Planning and Support:** Planning the resources for a release.
15. **Change Management:** Controlling the lifecycle of all changes (The 7 Rs).
16. **Service Asset and Configuration Management (SACM):** Managing the **CMDB** and **CIs**.
17. **Release and Deployment Management:** Moving changes into the live environment.
18. **Service Validation and Testing:** Ensuring the service meets requirements.
19. **Change Evaluation:** Assessing the performance of a change after implementation.
20. **Knowledge Management:** Ensuring the right info is available (includes the **KEDB**).

### **4. Service Operation (5 Processes)**

*Focus: Daily delivery and support (The "Engine Room" for MIM).*
21. **Event Management:** Monitoring CIs to identify state changes.
22. **Incident Management:** Restoring service ASAP (includes **MIM**).
23. **Request Fulfillment:** Handling Service Requests.
24. **Problem Management:** Finding the root cause (Reactive vs. Proactive).
25. **Access Management:** Granting or denying users access to services.

### **5. Continual Service Improvement (1 Process)**

*Focus: Incremental and large-scale improvements.*
26. **The 7-Step Improvement Process:** Identifying, defining, gathering, processing, analyzing, presenting, and implementing improvements.

---

## **The MIM "Survival" List**

As an entry-level MIM, you don't need to be an expert in all 26. You must master these **six** above all others:

1. **Incident Management:** Your primary function.
2. **Problem Management:** To ensure the fire doesn't restart.
3. **Change Management:** To authorize your emergency fixes.
4. **Service Asset & Configuration Management:** To understand the "Butterfly Effect" in the CMDB.
5. **Service Level Management:** To know how much "downtime" the business can tolerate (SLA).
6. **Knowledge Management:** To use and update the KEDB.

In the world of Major Incident Management, a **Change** is a controlled journey from a "proposed fix" to a "live solution."

Here is the step-by-step lifecycle of an **Emergency Change**, which is the most common type you will handle as an MIM.

---

## **The Step-by-Step Change Lifecycle**

### **Step 1: Request for Change (RFC) Submission**

The process begins when a technical team identifies a solution that requires a modification to the infrastructure.

* **The Action:** An engineer fills out a digital form (in a tool like ServiceNow or Jira) detailing what needs to move, add, or change.
* **The Example:** During a major website outage, the Cloud Team realizes the Load Balancer configuration is corrupted. They submit an RFC to "Revert Load Balancer to the last known stable configuration."

### **Step 2: Impact & Risk Assessment (The 7 Rs)**

The Change Manager (or the MIM in an emergency) evaluates the proposal using the **7 Rs** framework.

* **The Action:** You analyze the **CMDB** to see which other services might be affected (The Butterfly Effect).
* **The Example:** You ask, "If we revert this configuration, will it disconnect the users currently logged into the mobile app?"

### **Step 3: Authorization (ECAB Approval)**

Standard changes wait for a weekly meeting, but Emergency Changes need a "War Room" decision.

* **The Action:** You convene the **Emergency Change Advisory Board (ECAB)**—usually the MIM, a Technical Lead, and a Business Director—for a verbal "Go/No-Go."
* **The Example:** The Director of E-commerce provides verbal approval on the bridge at 10:15 PM because the cost of downtime outweighs the risk of the change.

### **Step 4: Implementation**

The change is applied to the live environment.

* **The Action:** The "Responsible" engineer executes the steps exactly as written in the RFC.
* **The Example:** The Cloud Engineer runs the script to restore the Load Balancer settings.

### **Step 5: Post-Implementation Review & Testing (PIR)**

We verify if the "Cure" worked without creating a new "Disease."

* **The Action:** QA or the MIM checks the service status. If the service is still down or worse, the **Back-out Plan** is triggered.
* **The Example:** You verify that the website is loading again and users can successfully check out.

### **Step 6: Closure & CMDB Update**

The final administrative step to ensure the "Map" matches the "Territory."

* **The Action:** The Change ticket is marked "Successful," and the **Configuration Item (CI)** record in the CMDB is updated with the new version details.
* **The Example:** The system now reflects that the Load Balancer is running "Config Version 2.4" instead of the corrupted "Version 2.5."

---

## **Example Scenario: The "Locked Out" Crisis**

| Step | Action Taken |
| --- | --- |
| **Problem** | 5,000 employees cannot log into the VPN (P1 Incident). |
| **RFC** | Security Team proposes an Emergency Change to bypass a faulty MFA (Multi-Factor Authentication) server. |
| **Risk (7 Rs)** | **Risk:** Lower security for 1 hour. **Return:** 5,000 people back to work. |
| **ECAB** | The Head of Security approves the temporary bypass. |
| **Execution** | The firewall rule is updated to redirect traffic. |
| **Back-out Plan** | "If traffic doesn't flow in 5 mins, we will re-enable the MFA block." |
| **Result** | Success. VPN access restored. |

---

### **MIM Pro-Tip: The "Golden Rule" of Changes**

As an entry-level MIM, always remember: **No Back-out Plan = No Approval.** Even in the middle of a crisis, you must never allow a change that can't be undone if it fails.

To help you distinguish between these two speeds of operation, here are two practical examples. Notice how the **Emergency** change focuses on speed and restoration, while the **Standard** change focuses on efficiency and pre-authorization.

---

## **Example 1: Emergency Change (ECR)**

**Scenario:** The company’s core Database is throwing "Connection Timeout" errors. All retail stores are unable to process customer payments.

* **Step 1: The Trigger (MIM Bridge)**
The Major Incident is active. Technical SMEs identify that the Primary Database is unresponsive.
* **Step 2: The Proposal (RFC)**
The Database Admin proposes an **Emergency Change** to failover to the Passive/Secondary Database node.
* **Step 3: Rapid Assessment (7 Rs)**
* **Reason:** Total payment outage.
* **Risk:** Potential 30-second data gap during the switch.


* **Step 4: ECAB Approval**
You (the MIM) call the IT Director. They provide verbal approval over the bridge to prioritize service restoration over the 30-second data risk.
* **Step 5: Implementation & Back-out**
The failover is executed. The **Back-out plan** is to point back to the Primary node if the Secondary fails to sync.
* **Step 6: Resolution**
Payments start flowing again. You document the change in the incident log and update the **CMDB** to show the Secondary node is now "Active."

---

## **Example 2: Standard Change**

**Scenario:** A department needs to update the antivirus software on 50 staff laptops. This is a routine, low-risk task performed every month.

* **Step 1: Pre-Authorization**
This type of change has been performed 100 times before without failure. It is already registered in the system as a "Standard Change."
* **Step 2: Logging (The RFC)**
The Desktop Support team logs a Change Ticket. Because it is "Standard," it **does not** need to go to a Change Advisory Board (CAB) meeting.
* **Step 3: Scheduling**
The team schedules the update for Friday at 6:00 PM to ensure zero business impact.
* **Step 4: Implementation**
The automated script pushes the antivirus update to the laptops.
* **Step 5: Automated Validation**
The system checks that all 50 laptops report "Success."
* **Step 6: Closure**
The ticket is closed automatically. No MIM involvement was required because there was no "unplanned interruption."

---

### **Key Differences for the MIM**

| Feature | **Emergency Change** | **Standard Change** |
| --- | --- | --- |
| **MIM Involvement** | **High:** You lead the decision. | **None:** It’s "Business as Usual." |
| **Approval** | Immediate (ECAB). | Pre-approved by policy. |
| **Timing** | Right now (to fix a "Fire"). | Scheduled (to maintain the "House"). |
| **Risk** | High (could cause a Butterfly Effect). | Extremely Low (proven history). |

---

### **Final Documentation Summary**

You now have a complete, professional guide covering the entire ITIL lifecycle from an MIM perspective. You have:

1. The **Definitions** (Incident, Problem, Change).
2. The **Workflow** (Butterfly Investigation, 5 Whys, Fishbone).
3. The **Governance** (7 Rs, KEDB, CMDB).
4. The **Real-World Examples** (Emergency vs. Standard).

In a professional IT Service Management (ITSM) environment, a failed change is one of the most common triggers for both a **Major Incident** and a subsequent **Problem Ticket**.

When a change fails, it means the "solution" intended to improve the system actually caused a new "unplanned interruption."

---

## **The Failed Change Workflow**

### **1. The Incident Trigger (Reactive)**

If a Change (Standard, Normal, or Emergency) is implemented and immediately causes a service outage:

* **MIM Action:** You must immediately declare a **Major Incident**.
* **The First Priority:** Execute the **Back-out Plan** (Rollback) to restore the previous stable state of the Configuration Item (CI).

### **2. Creating the Problem Ticket**

Once the service is restored (or even while the outage is active), a **Problem Ticket** is created specifically for this failed change.

**Why create a Problem ticket for a failed change?**

* **To Investigate the "Why":** Why did a change that was tested and approved fail in the live environment?
* **Post-Implementation Review (PIR):** To identify if the failure was due to a technical bug, incorrect CMDB data, or human error during implementation.
* **Preventing Recurrence:** To update the **Change Management** process so that similar changes don't fail in the future.

---

## **Example: From Failed Change to Problem Ticket**

| Stage | Action |
| --- | --- |
| **The Change** | An engineer implements a "Normal Change" to upgrade the company’s firewall firmware at 2:00 AM. |
| **The Failure** | At 2:05 AM, all internet traffic to the headquarters drops. The change has failed. |
| **MIM Response** | You are paged. You order an immediate **Rollback**. The engineer reverts the firmware to the previous version. Service is restored by 2:15 AM. |
| **Problem Creation** | You log a **Problem Ticket** linked to that specific Change Request (CR) and the Firewall **CI**. |
| **Investigation** | The Problem Manager uses the **5 Whys**: *Why did it fail?* The new firmware wasn't compatible with the specific hardware model recorded in the **CMDB**. |
| **KEDB Update** | A "Known Error" is created: *"Do not apply Firmware v5.2 to Router Model X; leads to immediate port shutdown."* |

---

## **The "Butterfly Effect" Connection**

A failed change is the ultimate example of the **Butterfly Effect**. A small line of code in an authorized update can crash an entire global business service.

* **The MIM's Role:** During the Problem investigation, you help identify if the "Butterfly Investigation" performed during the Change assessment was insufficient.
* **The Goal:** Turn the "Failed Change" into a "Learning Opportunity" that improves the **Standard Operating Procedures (SOPs)**.

---

### **Professional Summary for your Documentation:**

> "A failed change is a high-priority trigger for Problem Management. It necessitates a formal investigation to determine whether the failure was a result of poor testing, inaccurate CMDB dependency mapping, or an unforeseen technical conflict, ensuring future changes are executed with higher confidence."
