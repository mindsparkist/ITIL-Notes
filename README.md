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


