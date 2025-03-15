# Introduction to IT Service Management (ITSM)

## What is ITSM?
IT Service Management (ITSM) is the practice of implementing, managing, and delivering IT solutions that align with business objectives.

### Key Pillars of ITSM:
- **Users**
- **Services**
- **Quality**
- **Cost**

### Real-World Example
Customers report incidents to an IT support company. Platforms like ServiceNow offer a user-friendly interface to log and manage these incidents efficiently, benefiting both service providers and customers.

## ITSM Framework
### ITIL – Information Technology Infrastructure Library
ITIL is a best-practice framework for delivering IT services efficiently. Developed by the British government, it provides structured guidelines for IT service management.

### Steps of ITIL
*(Insert relevant images here)*

---
## Hands-On ServiceNow (SNOW)
ServiceNow is a cloud-based platform that provides ITSM solutions, helping organizations automate IT services, operations, and workflows.

### How to Obtain a Personal Instance of SNOW
*(Insert image link here)*

---
## Incident & Major Incident Management

### What is a Major Incident?
*(Insert relevant images here)*

### Key Stakeholders (Personas)
*(Insert relevant diagram here)*

### Incident Management Flow
*(Insert relevant diagram here)*

### Step-by-Step Guide to Creating an Incident
1. In ServiceNow, navigate to **Create New Incidents**.
2. The **Incident Number** is automatically generated and stored in the database.
3. **Configuration Item (CI)** relates to the **Configuration Management Database (CMDB)**.

### Incident Lifecycle:
- **New:** The incident has been reported but not reviewed.
- **In Progress:** Being actively worked on.
- **On Hold:** Temporarily paused, awaiting more information or third-party response.
- **Resolved:** Addressed with a solution.
- **Closed:** Confirmed as resolved, no further action required.

Formula: **Priority = Impact + Urgency**

After creating an incident:
1. Fill out resolution details.
2. Resolve the ticket.
3. The ticket automatically closes after a predefined period (e.g., 5 days).

*(Insert process diagram here)*

### Major Incident Process
1. **Install the Major Incident Plugin** (if not already installed).
2. **Promoting an Incident to a Major Incident:**
   - Assess if multiple users are affected.
   - The incident manager or an experienced helpdesk agent can propose a promotion.
   - Document the reason for promotion.
   - Add work notes and business impact details.
3. **Demoting a Major Incident** (if found unnecessary).
4. **Proposing Before Promotion:**
   - Incident enters **Proposed State**.
   - Major incidents are assigned to a specialized team.
   - The Major Incident Management Team reviews the incident.
5. **Final Decision:**
   - If valid, the incident is promoted to a Major Incident.
   - Otherwise, it is demoted.

*(Insert relevant screenshots and diagrams here)*

---
## Workbench in Major Incident Management
Workbench consists of two primary tabs:
1. **Summary Tab** – Provides an overview, allowing managers to add Configuration Items (CIs), child tickets, and affected locations.
2. **Communication Tab** – Used to send email notifications using predefined templates.

### Managing Communication
1. Set up email communication by adding communication tasks.
2. Define the communication plan and recipients.
3. Save and send emails to the relevant teams.

*(Insert workbench UI screenshot here)*

---
## Problem Management

### Example Scenario
**Incident:** A user experiences a **Blue Screen of Death (BSOD)**. The issue persists despite multiple reboots.

#### Investigation Process:
1. Log the incident in the ITSM system.
2. Perform basic hardware diagnostics.
3. Analyze the BSOD error codes, pointing to possible software corruption.

#### Immediate Resolution:
1. **Reinstall the Operating System** – User data is backed up and restored.
2. **Monitor System Stability** – Ensure issue does not recur.

#### Root Cause Analysis:
1. **Software Audit:** Identified unauthorized software (e.g., torrent client).
2. **Policy Enforcement:** Updated endpoint protection to block unauthorized applications.
3. **User Education:** Explained policies to prevent recurrence.

#### Follow-Up:
- **Monitoring:** The system was tracked for further issues.
- **Feedback:** The user provided positive feedback.

*(Insert problem management process diagram here)*

---
## Request Fulfillment
### What is Request Fulfillment?
Handling service requests such as hardware and software requests.

### Process Overview:
1. A **Request Ticket (REQ)** is created.
2. A **Request Item (RITM)** is generated.
3. Tasks (SCTASK) are completed to fulfill the request.
4. The RITM progresses as SCTASKs are resolved.

*(Insert screenshots and diagrams here)*

---
## Change Management
### Types of Changes
1. **Standard Change:** Pre-approved, low risk (e.g., routine software updates).
2. **Normal Change:** Requires Change Advisory Board (CAB) approval.
3. **Emergency Change:** Implemented urgently to resolve critical issues (e.g., security vulnerabilities).

### Change Advisory Board (CAB)
A team responsible for evaluating and approving changes.

### Change Management Workflow
*(Insert process diagram here)*

#### Raising a Change from a Problem Ticket
1. Right-click on the Problem Ticket and select **Create Normal Change**.
2. Fill out required details and request approval.
3. Once approved, the change state updates to **Scheduled**.
4. After implementation, a **Review Phase** is conducted.

*(Insert screenshots and process flow diagrams here)*

---
## Configuration Management Database (CMDB)
CMDB stores Configuration Items (CIs) and their relationships.

### Example:
- HR department requires a database for employee records.
- The database is stored on a hard disk and is accessible to employees.
- CMDB provides an organized view of IT assets and dependencies.

*(Insert CMDB UI screenshot here)*

---
## Knowledge Management
### Creating a Knowledge Article
1. Navigate to **Knowledge Section** in SNOW.
2. Click **Knowledge Bases > New**.
3. Fill in required fields and assign an **Owner**.
4. Save and publish the article.
5. The article is accessible to agents and end users.

*(Insert screenshots of knowledge base creation here)*

---
## Service Level Management
### Understanding SLAs, OLAs, and UCs
- **SLA (Service Level Agreement):** Agreement with customers on service response times.
- **OLA (Operational Level Agreement):** Internal agreements ensuring SLAs are met.
- **UC (Underpinning Contract):** Vendor agreements for software/hardware delivery.

### Creating SLAs in SNOW
1. Search for **SLA Definitions**.
2. Click **New**.
3. Name the SLA, set **Target**, and define **Conditions**.
4. Configure **Duration**, **Schedule**, and **Time Zone**.

*(Insert SLA UI screenshots here)*

---
### End of Document

