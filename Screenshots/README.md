# Civic System — Implementation Evidence

This directory contains selected screenshots demonstrating the implementation, integration and testing of the **Civic System – PCC Service Assistant** portfolio prototype.

Civic System is an independent public-sector AI prototype developed to demonstrate how Microsoft Copilot Studio and the Power Platform can support council-service information, grounded knowledge retrieval, controlled service workflows and human escalation.

> **Important:** Civic System is a portfolio prototype and is **not an official Portsmouth City Council service**. It does not connect to Portsmouth City Council's internal systems.

## Screenshot Evidence

### 01 — Copilot Studio Agent

**File:** `01-copilot-agent.png`

Shows the Civic System agent configured in Microsoft Copilot Studio, including the main agent development environment used to build and test the conversational assistant.

Demonstrates:
- Microsoft Copilot Studio
- Conversational AI development
- Agent configuration
- Generative AI instructions
- Public-service conversational design

---

### 02 — Knowledge Base

**File:** `02-knowledge-base.png`

Shows the approved knowledge sources connected to Civic System.

The knowledge base contains 22 resident-facing documents covering:

- Council Tax
- Waste and Recycling
- Housing
- General Council Services
- Adult Social Care
- Parking
- Benefits and Support

These sources provide the grounding information used by the agent when answering resident enquiries.

Demonstrates:
- Knowledge management
- Grounded AI
- Retrieval-Augmented Generation (RAG)
- Controlled information sources
- Public-sector information architecture

---

### 03 — Copilot Skills

**File:** `03-copilot-skills.png`

Shows the service-specific skills configured within Civic System.

The agent uses dedicated skills for:

- Council Tax Support
- Waste and Recycling Support
- Housing Support
- General Services Support
- Adult Social Care Support
- Parking Support
- Benefits and Support
- Safety, Fallback and Escalation

Demonstrates:
- Intent routing
- Modular conversational architecture
- Service-specific AI behaviour
- Safety and escalation controls

---

### 04 — RAG Grounded Response

**File:** `04-rag-grounded-response.png`

Shows Civic System retrieving relevant information from its approved knowledge base and generating a grounded response.

The tested scenario required information from more than one knowledge source, demonstrating cross-document retrieval and multi-service reasoning.

Demonstrates:

**Resident Query → Agent → Relevant Skill → Knowledge Retrieval → Grounded Response → Safety Check → Resident Answer**

This provides evidence of the project's Retrieval-Augmented Generation architecture.

---

### 05 — Service Issue Workflow

**File:** `05-service-issue-workflow.png`

Shows the Power Automate workflow:

**CivicSystem - Submit Service Issue**

The workflow receives information collected by the Copilot Studio agent, creates a prototype reference number and writes the service request to Microsoft Dataverse.

Example architecture:

**Copilot Studio → Power Automate → Dataverse → Workflow Response**

The agent requires explicit resident confirmation before invoking the transaction workflow.

Demonstrates:
- Power Automate
- Workflow automation
- Transaction controls
- Dataverse integration
- Reference generation
- AI-to-backend integration

---

### 06 — Human Support Workflow

**File:** `06-human-support-workflow.png`

Shows the Power Automate workflow:

**CivicSystem - Request Human Support**

The workflow provides a controlled route for escalating an enquiry from the AI assistant to a human-review process.

Information captured includes:

- Service area
- Reason for escalation
- Resident request
- Contact preference
- Status
- Prototype escalation reference

Demonstrates:
- Human-in-the-loop AI
- Escalation workflow design
- Responsible AI
- Power Automate
- Dataverse integration

---

### 07 — Dataverse Service Request

**File:** `07-dataverse-service-request.png`

Shows a successfully created prototype service-request record stored in Microsoft Dataverse.

The service-request data model includes:

- Reference Number
- Issue Type
- Issue Description
- Location
- Status
- Submitted Date

This demonstrates that a transaction initiated through the conversational interface can be processed by Power Automate and persisted in the application's data layer.

Demonstrates:

**Conversational AI → Workflow → Structured Data Persistence**

---

### 08 — Power Apps Staff Portal

**File:** `08-staff-portal.png`

Shows the **Civic System – Staff Portal**, developed as a Microsoft Power Apps model-driven application.

The portal provides staff-facing access to:

1. Civic Service Requests
2. Civic Human Support Requests

This completes the prototype's end-to-end architecture:

**Resident**
↓  
**Microsoft Copilot Studio**
↓  
**RAG / Service Skills**
↓  
**Power Automate**
↓  
**Microsoft Dataverse**
↓  
**Power Apps Staff Portal**
↓  
**Human Review**

---

## Technologies Demonstrated

The screenshots provide implementation evidence across:

- Microsoft Copilot Studio
- Generative AI
- Prompt Engineering
- Retrieval-Augmented Generation (RAG)
- Knowledge Management
- Power Automate
- Microsoft Dataverse
- Power Apps
- Model-Driven Apps
- Conversational AI
- Workflow Automation
- Human-in-the-Loop AI
- Responsible AI
- Data Minimisation
- Transaction Controls
- Public-Sector Digital Service Design

## Testing

Civic System was evaluated through **23 recorded prototype test scenarios**, covering areas including:

- Knowledge retrieval
- Cross-document RAG
- Hallucination resistance
- Prompt-injection handling
- Information versus transaction control
- Privacy and data minimisation
- Missing-information handling
- Explicit transaction confirmation
- Workflow execution
- Dataverse persistence
- Human escalation
- Private-account boundaries
- Out-of-scope handling
- Unsupported claims
- Staff Portal integration

All **23 recorded scenarios passed within the defined prototype test set**.

This result represents portfolio prototype testing and should **not** be interpreted as production certification.

## Accessibility and Responsible AI

The project also evaluated relevant accessibility and inclusive-design principles, including:

- Plain English
- Progressive disclosure
- Error tolerance
- Low digital-confidence support
- Typing-error tolerance
- Human escalation

Responsible AI controls include:

- Transparency
- Human oversight
- Grounded responses
- Privacy and data minimisation
- Fairness
- Safety and escalation
- Accountability and auditability
- Clear AI decision boundaries

## Security and Privacy

Screenshots are provided solely as portfolio implementation evidence.

Sensitive information such as:

- Passwords
- Authentication credentials
- Access tokens
- Connection secrets
- Private resident information
- Payment credentials

has not intentionally been included.

## Disclaimer

**Civic System is an independent portfolio prototype created to demonstrate AI and Microsoft Power Platform engineering capabilities.**

It is **not an official Portsmouth City Council application or service**, does not represent Portsmouth City Council, and does not claim access to the council's internal systems.

Any `CIVIC-` or `ESC-` references displayed in the screenshots are **prototype Civic System references and are not official Portsmouth City Council case or reference numbers**.
