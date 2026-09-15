# Civic System — Microsoft Power Platform Solution

This directory contains the exported Microsoft Power Platform solution package for the **Civic System – PCC Service Assistant** portfolio prototype.

## Project Overview

Civic System is an independent AI-enabled public-sector services prototype designed to demonstrate how conversational AI and Microsoft Power Platform technologies can be combined to support council-service information, controlled transactions, workflow automation and human escalation.

The solution was developed using:

- Microsoft Copilot Studio
- Generative AI
- Retrieval-Augmented Generation (RAG)
- Power Automate
- Microsoft Dataverse
- Power Apps
- Model-driven applications

> **Important:** Civic System is an independent portfolio prototype. It is not an official Portsmouth City Council application or service.

---

## Exported Solution

The ZIP file in this directory is the exported Microsoft Power Platform solution package created from the project's development environment.

The package is provided to demonstrate the underlying Power Platform implementation and to complement the project documentation and implementation screenshots available elsewhere in this repository.

**Do not extract or modify the contents of the exported ZIP package before importing it into Power Platform.**

---

## Solution Architecture

The prototype implements the following end-to-end architecture:

Resident / User  
↓  
Microsoft Copilot Studio  
↓  
Service Skills & Conversational Routing  
↓  
Retrieval-Augmented Generation (RAG)  
↓  
Approved Knowledge Sources  
↓  
Power Automate Workflows  
↓  
Microsoft Dataverse  
↓  
Power Apps Staff Portal  
↓  
Human Review

---

## Core Solution Components

### 1. Microsoft Copilot Studio Agent

The **Civic System – PCC Service Assistant** provides the conversational interface.

The agent was designed to:

- Identify the resident's service requirement
- Route enquiries to appropriate service skills
- Retrieve information from approved knowledge sources
- Generate grounded responses
- Distinguish information requests from transactions
- Collect required information before transactions
- Require confirmation before workflow execution
- Escalate appropriate enquiries for human review
- Apply privacy, safety and Responsible AI controls

---

### 2. Service Skills

Civic System contains dedicated conversational capabilities covering:

1. Council Tax
2. Waste and Recycling
3. Housing
4. General Council Services
5. Adult Social Care
6. Parking
7. Benefits and Support
8. Safety, Fallback and Escalation

These skills provide modular service routing and help prevent unrelated service logic from being mixed together.

---

### 3. Retrieval-Augmented Generation (RAG)

The agent uses approved knowledge sources to ground its responses.

The core retrieval architecture is:

User Query  
→ Intent Identification  
→ Relevant Service Skill  
→ Approved Knowledge Retrieval  
→ Relevant Document Content  
→ Grounded Generative Response  
→ Safety and Boundary Checks  
→ User Response

The project knowledge base contains **22 resident-facing knowledge documents** across the supported service areas.

Additional governance documentation defines knowledge management, retrieval standards, lifecycle management, quality controls and privacy requirements.

---

### 4. Service Issue Workflow

The Power Automate workflow:

`CivicSystem - Submit Service Issue`

supports controlled prototype service-request submission.

The workflow captures information including:

- Issue type
- Issue description
- Location
- Contact preference

A prototype reference is generated after successful workflow execution.

Example:

`CIVIC-YYYYMMDD-HHMMSS`

The workflow stores the resulting service request in Microsoft Dataverse.

The conversational agent must receive explicit user confirmation before executing the workflow.

---

### 5. Human Support Workflow

The Power Automate workflow:

`CivicSystem - Request Human Support`

provides a human-in-the-loop escalation mechanism.

The workflow can capture:

- Service area
- Reason for escalation
- Resident request
- Contact preference
- Status
- Submission information

A successful escalation generates a prototype `ESC-` reference.

These references are Civic System prototype identifiers and are **not official Portsmouth City Council case numbers**.

---

## Microsoft Dataverse

Dataverse provides the structured data layer for the prototype.

### Civic Service Requests

The service-request data model includes:

- Reference Number
- Issue Type
- Issue Description
- Location
- Status
- Submitted Date

### Civic Human Support Requests

The human-support data model includes:

- Escalation Reference
- Service Area
- Reason for Escalation
- Resident Request
- Contact Preference
- Status
- Submitted Date

---

## Power Apps Staff Portal

The project includes the model-driven application:

**Civic System – Staff Portal**

The Staff Portal provides staff-facing access to:

- Civic Service Requests
- Civic Human Support Requests

This demonstrates the full prototype integration between the resident-facing conversational assistant and a staff-facing operational interface.

---

## Transaction Controls

Civic System separates information requests from transactional requests.

A transaction is not executed simply because a user mentions an issue.

For service submissions, the prototype follows the pattern:

Identify Request  
→ Gather Required Information  
→ Explain Proposed Submission  
→ Request User Confirmation  
→ Execute Workflow  
→ Verify Workflow Result  
→ Return Prototype Reference

The agent must not claim that a transaction succeeded unless the connected workflow returns successful confirmation.

---

## Human-in-the-Loop Design

Civic System does not make significant legal, financial, welfare, statutory or eligibility decisions.

Human oversight remains necessary for areas including:

- Council Tax liability
- Benefit entitlement
- Statutory homelessness decisions
- Adult Social Care eligibility
- Safeguarding decisions
- Parking challenge outcomes
- Complex complaints
- Other cases requiring authorised professional judgement

The AI is designed primarily to support information retrieval, service navigation, structured data collection and controlled workflow initiation.

---

## Responsible AI

Responsible AI principles incorporated into the prototype include:

- Transparency
- Grounded AI responses
- Human oversight
- Privacy and data minimisation
- Fairness and non-discrimination
- Safety and escalation
- Accountability
- Auditability
- Clear AI decision boundaries

The agent must not fabricate council policies, case information, transactions, reference numbers or eligibility decisions.

---

## Testing

The complete Civic System prototype was evaluated using **23 recorded test scenarios**.

Testing covered:

- RAG and cross-document retrieval
- Hallucination resistance
- Prompt-injection handling
- Transaction safety
- Statutory decision boundaries
- Cross-service routing
- Safeguarding
- Workflow execution
- Dataverse persistence
- Workflow failure handling
- Human escalation
- Staff Portal integration
- Information versus transaction handling
- Privacy and data minimisation
- Missing-information handling
- Explicit transaction confirmation
- Private-account boundaries
- Out-of-scope handling
- Unsupported claims and uncertainty

All **23 recorded scenarios passed within the defined prototype test set**.

This result represents prototype portfolio testing and **does not constitute production certification**.

---

## Import Considerations

The exported solution is provided primarily as portfolio and technical implementation evidence.

Importing the solution into another Microsoft Power Platform environment may require additional configuration, including:

- Appropriate Microsoft licences
- Dataverse availability
- Security roles and permissions
- Connection references
- Power Automate connections
- Environment-specific configuration
- Copilot Studio configuration
- Knowledge-source configuration
- Authentication
- Data Loss Prevention policies

Environment-specific connections, credentials and authentication information are intentionally not distributed with the portfolio.

---

## Security

This repository must not contain:

- Passwords
- API secrets
- Authentication tokens
- Private connection credentials
- Payment information
- Real resident personal information
- Confidential council information

The exported package is included only as evidence of the technical implementation.

---

## Repository Evidence

Additional project evidence is available in the main repository:

- `/docs` — Complete project and technical documentation
- `/screenshots` — Implementation screenshots
- `/solution` — Exported Power Platform solution
- `README.md` — Full project overview and architecture

Together, these provide evidence of the project's design, development, integration, testing and governance.

---

## Disclaimer

**Civic System is an independent portfolio prototype developed to demonstrate Microsoft Copilot Studio, Generative AI, RAG and Power Platform engineering capabilities.**

It is **not an official Portsmouth City Council service**, is not endorsed by Portsmouth City Council, and does not represent or provide access to Portsmouth City Council's production systems.

Any `CIVIC-` or `ESC-` reference numbers generated by the prototype are demonstration references only and must not be interpreted as official Portsmouth City Council case or transaction references.
