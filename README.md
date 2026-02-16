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

