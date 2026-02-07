Problem Management is the ITIL process responsible for managing the lifecycle of all "Problems"—defined as the underlying or unknown root causes of one or more incidents. While Incident Management (and MIM) focuses on the immediate "symptoms," Problem Management focuses on the "disease" to prevent future disruptions.

The Relationship Between MIM and Problem Management
The two processes operate in a symbiotic, yet distinct, relationship often described as the "Firefighter vs. Fire Investigator" model:

Handover of Intelligence: Once a Major Incident is restored, the MIM hands over the "body of evidence"—including logs, diagnostic data, and applied workarounds—to the Problem Management team.

Root Cause Analysis (RCA): Problem Management performs a deep-dive investigation into the MI to identify why the failure occurred.

KEDB Integration: Any "Workaround" found by the MIM during the bridge is documented by Problem Management in the Known Error Database (KEDB) for future reference.

Proactive Prevention: Problem Management uses trend analysis to identify if an incident is recurring multiple times, triggering an investigation even if a single Major Incident hasn't occurred.

The Strategic Workflow
To maintain professional standards in your documentation, frame the interaction as a three-step cycle:

Major Incident (The Symptom): The service is down; the MIM restores it via a workaround.

Problem (The Cause): Investigation reveals the structural root cause of the outage.

Change (The Cure): A permanent fix is implemented via Change Management to modify the Configuration Item (CI) and update the CMDB.

In the ITIL framework, the KEDB (Known Error Database) is the bridge between past failures and future solutions. It serves as a repository for documented issues that have a known root cause and a validated workaround.

What is the KEDB?
The Known Error Database is a database maintained by Problem Management that stores "Known Errors"—incidents or problems for which the root cause is understood, but a permanent fix (Change) has not yet been implemented.

How KEDB is used in MIM and Problem Management
The KEDB acts as the "shared memory" between reactive and proactive teams:

In Major Incident Management (MIM): When a Major Incident occurs, the MIM immediately searches the KEDB to see if the symptoms match a previously documented "Known Error." If a match is found, the MIM can apply the pre-verified Workaround instantly, significantly reducing the Mean Time to Repair (MTTR) without waiting for technical teams to reinvent the solution.

In Problem Management: Once a Problem Manager identifies a root cause but cannot immediately apply a permanent fix (perhaps due to cost or technical constraints), they create a Known Error Record in the KEDB. This ensures that if the incident recurs, the organization is prepared to handle it efficiently.

Feature,KEDB (Known Error Database),CMDB (Configuration Management Database)
Primary Content,"Historical errors, root causes, and workarounds.","Assets, Configuration Items (CIs), and their relationships."
Focus,"""What went wrong and how do we bypass it?""","""What do we own and how is it connected?"""
The Connection,A Known Error in the KEDB is almost always linked to a specific CI in the CMDB.,"The CMDB provides the ""map"" to understand which services will be affected by a Known Error."

Reactive Problem Management
Reactive Problem Management is triggered in response to a specific incident that has already occurred. It is the "fire investigation" that follows the "firefighting" of the Major Incident.

Trigger: Typically initiated following a Major Incident or a series of recurring incidents.

Objective: To identify the root cause of a past disruption and ensure it does not happen again.

Example: A payment gateway fails for three hours (Major Incident). Reactive Problem Management is initiated to perform a Root Cause Analysis (RCA), discovering that a specific server's memory was overloaded due to a code bug.

Proactive Problem Management
Proactive Problem Management is initiated as part of continuous service improvement. It looks for patterns and potential failures before they manifest as a Major Incident.

Trigger: Initiated by trend analysis, log reviews, or health checks of Configuration Items (CIs) in the CMDB.

Objective: To identify and eliminate structural weaknesses or "vulnerabilities" in the IT infrastructure before they cause a disruption.

Example: A Problem Manager notices that a database's CPU usage has been slowly increasing by 5% every week (Trend Analysis). Even though no outage has occurred yet, they investigate and find a "memory leak," which they fix via a scheduled Change to prevent a future crash.

Feature,Reactive,Proactive
Mindset,"""Why did it break?""","""What might break next?"""
Timing,Post-Incident.,Pre-Incident.
Data Source,Incident Logs and Transcripts.,Monitoring tools and Trend Reports.
Value,Prevents recurrence of known issues.,Increases overall system availability and stability.

When is a Problem Ticket Created?
A Problem Ticket is typically generated under the following conditions:

Major Incident Follow-up: Automatically triggered after a P1 or P2 incident is resolved to perform a Root Cause Analysis (RCA).

Recurring Incidents: When multiple low-priority incidents show a similar pattern (e.g., three people reporting the same software crash).

Proactive Analysis: When trend analysis or monitoring tools identify a vulnerability or performance degradation before an outage occurs.

Unresolved Incidents: When a workaround has been applied but the incident remains "open" because the underlying cause is unknown.

The Problem Management Lifecycle
The lifecycle moves from identification to permanent resolution.

1. Detection & Logging
The problem is identified via reactive or proactive channels and logged as a "Problem Record."

2. Categorization & Prioritization
Categorization: Linked to the correct Configuration Item (CI) in the CMDB (e.g., specific server, application, or network switch).

Prioritization: Assigned a priority based on the business impact and the frequency of the related incidents.

3. Investigation & Diagnosis
The Problem Manager and Subject Matter Experts (SMEs) use techniques like the "Five Whys" or Ishikawa (Fishbone) diagrams to find the technical root cause.

Workaround Identification: If a workaround is found, it is published to the KEDB for immediate use by the MIM.

4. Establishing a Known Error
Once the root cause is found but the fix isn't yet implemented, the record is transitioned to a Known Error. This informs the Service Desk and MIM that the "Problem" is understood.

5. Resolution & Closure
Change Request (CR): Most problems require a Change Management ticket to apply a permanent fix (e.g., a hardware replacement or code patch).

Validation: After the change is implemented, the team monitors the service to ensure the incidents do not return.

Closure: The Problem Ticket is closed, and the KEDB is updated to reflect the permanent resolution.

How it is Handled: Key Roles
Problem Manager: Owns the lifecycle, coordinates meetings, and ensures RCAs are completed on time.

Subject Matter Experts (SMEs): Provide the technical deep-dive and perform the actual repair.

MIM (Major Incident Manager): Provides the initial data and incident logs to start the investigation.

In the **Investigation & Diagnosis** phase of Problem Management, the goal is to move beyond symptoms to identify the true root cause. Two of the most effective professional techniques for this are **Fishbone Diagrams** and **The 5 Whys**.

---

## **1. The Fishbone (Ishikawa) Diagram**

The Fishbone diagram is a visual brainstorming tool used to categorize the potential causes of a Major Incident. It helps the MIM and SMEs ensure they aren't overlooking any part of the IT ecosystem.

### **The "6 Ms" Categories for IT:**

To identify where the "Butterfly Effect" originated, technical teams analyze these categories:

* **Methods:** Were there flaws in the SOP or Change Management process?
* **Machines:** Is there a hardware failure in a specific **Configuration Item (CI)**?
* **Software (Material):** Was there a recent code deployment or a bug in the application?
* **Measurements:** Did the **Event Management** tools fail to provide accurate data?
* **Mother Nature (Environment):** Were there external factors like power outages or data center cooling issues?
* **Manpower:** Was the incident caused by human error during a manual configuration?

---

## **2. The 5 Whys Technique**

While the Fishbone diagram explores the **breadth** of potential causes, the **5 Whys** explores the **depth** of a specific failure. By repeatedly asking "Why," you peel away layers of symptoms to find the structural problem.

### **Example: A Major Database Outage**

1. **Why is the service down?** The database has crashed.
2. **Why did the database crash?** The disk space reached 100% capacity.
3. **Why was the disk full?** A log file grew unexpectedly large due to an error loop.
4. **Why did the error loop occur?** A recent **Change** was implemented without a proper health check.
5. **Why was it implemented without a check?** (Root Cause) The Standard Operating Procedure (SOP) for that specific CI was outdated in the **CMDB**.

---

## **How these relate to the MIM Process**

* **MIM Role:** During the "Butterfly Investigation," you use these techniques to guide the SMEs on the bridge.
* **Problem Management Role:** After service restoration, the Problem Manager formalizes these findings into the **Root Cause Analysis (RCA)** report.
* **KEDB Update:** Once the "5th Why" is identified, the **Known Error Database** is updated so that future MIMs can identify the issue faster.

A **Fishbone (Ishikawa) Diagram** is a structured visualization tool used to brainstorm and categorize the potential causes of a problem. In an ITIL context, it is essential for identifying the "Butterfly Effect"—how a failure in one area can cascade into a Major Incident.

Below is a professional, generic template tailored for IT Service Management.

---

## **Generic Fishbone (Ishikawa) Template: IT Service Failure**

### **1. The Problem Statement (The "Head")**

* **Definition:** Clearly state the Major Incident or service disruption being investigated.
* **Example:** "Total outage of the Global Payment Gateway affecting APAC transactions."

---

### **2. The Categories (The "Bones")**

#### **A. Systems & Infrastructure (Machines)**

* **Hardware Failure:** Server, router, or switch hardware malfunctions.
* **Resources:** Overloaded CPU, memory leaks, or exhausted disk space.
* **Connectivity:** Network latency, firewall blocks, or ISP outages.

#### **B. Processes & Procedures (Methods)**

* **Change Management:** Was a recent change implemented without proper testing?
* **SOP Accuracy:** Are the Standard Operating Procedures in the CMDB outdated?
* **Monitoring:** Did Event Management tools fail to trigger an alert?.

#### **C. Software & Data (Material)**

* **Code Bugs:** Recent application deployments or script errors.
* **Data Integrity:** Corrupted database tables or expired API certificates.
* **Third-Party Services:** Failures in external vendor APIs or cloud providers.

#### **D. People & Skills (Manpower)**

* **Human Error:** Incorrect manual configurations or unauthorized changes.
* **Skill Gaps:** Lack of Subject Matter Expertise (SME) for a specific technology.
* **Communication:** Delays in hierarchical or functional escalation.

#### **E. Measurements (Metrics)**

* **Thresholds:** Incorrectly set alert thresholds leading to "alert fatigue".
* **Logging:** Incomplete logs preventing rapid diagnosis.
* **KPIs:** Misalignment between technical performance and business SLAs.

#### **F. Environment (Mother Nature)**

* **Facility Issues:** Power outages, cooling failures, or physical damage in the data center.
* **External Factors:** Security breaches, DDoS attacks, or regional fiber cuts.

---

### **3. Analysis Phase**

* **Correlation:** Once all potential causes are plotted, the team identifies the most likely "bones" to investigate further.
* **The 5 Whys:** Apply the **5 Whys** technique to the most probable causes to drill down to the actual root cause.

### **Professional Summary for your Documentation:**

> "The Fishbone template provides a 360-degree view of the IT ecosystem, ensuring that the investigation covers all possible variables from technical infrastructure to human process. It is the primary tool for moving an incident from a 'Symptom' in the KEDB to a 'Root Cause' in a Problem Record".

