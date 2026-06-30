# AI Procurement Automation

> **An engineering-driven procurement automation platform that streamlines the complete procurement lifecycle using intelligent document processing, deterministic business logic, and professional document generation.**

---

## Why This Project Exists

Procurement is one of the most repetitive and detail-sensitive operations inside many engineering, manufacturing, and industrial companies.

A single Request for Quotation (RFQ) often starts a chain of repetitive manual tasks:

* Opening and reading incoming emails.
* Extracting dozens of part numbers manually.
* Rewriting information into spreadsheets.
* Looking up existing parts.
* Preparing quotation sheets.
* Contacting multiple suppliers individually.
* Waiting for supplier responses.
* Constantly checking emails to see who has replied.
* Remembering who still hasn't responded.
* Creating comparison sheets manually.
* Presenting quotations to engineers or managers for the final decision.

Although every one of these tasks appears simple, they consume a considerable amount of engineering time and introduce unnecessary opportunities for human error.

This project was not designed to automate isolated tasks.

It was designed to automate the **entire procurement lifecycle** while keeping every stakeholder informed, maintaining complete visibility over every order, and producing professional outputs that reflect the company's image.

The objective was never to build "an AI workflow."

The objective was to build a procurement platform around real business operations.

---

# Design Philosophy

Throughout the development of this system, one principle remained constant:

> **Every component exists because it solves a real business problem.**

No feature was added simply because it looked impressive.

Every workflow, every database table, every code node, every notification, every generated document and every design decision was created to improve reliability, reduce human effort, eliminate unnecessary mistakes or improve the experience of the people interacting with the system.

Whenever a technical decision conflicted with business usability, business usability came first.

---

# Business Capabilities

Instead of automating individual actions, the platform manages the procurement process from the moment an RFQ is received until the engineer receives a professionally organized quotation comparison.

The system currently provides:

* Multi-format RFQ processing.
* Intelligent document classification.
* AI-assisted data extraction.
* Database-backed part validation.
* Automatic RFQ generation.
* Professional Excel document creation.
* Supplier selection through simple commands.
* Automated supplier communication.
* Supplier response tracking.
* Deadline management.
* Procurement state tracking.
* Executive-ready comparison sheets.
* Complete order visibility.
* Real-time notifications.

Each capability exists for a specific operational reason.

The following sections explain those decisions in detail.

---

# Multi-Format RFQ Processing

Procurement departments rarely receive quotation requests in one standardized format.

Different clients work differently.

Some send professionally prepared Excel sheets.

Others attach PDFs.

Some simply write the required parts inside the email.

Many suppliers and customers even send screenshots or images.

Instead of forcing employees to manually rewrite every request into a structured format, the platform accepts:

* Excel
* PDF
* Plain text
* Images

Supporting image-based RFQs is particularly valuable.

Without automated extraction, employees often need to manually type every part number, description and quantity before any procurement work can even begin.

That repetitive task adds no business value while introducing opportunities for typing mistakes.

By supporting multiple formats from the beginning, the workflow adapts to the client's preferred communication method rather than forcing clients to adapt to the system.

---

# AI Used Where It Adds Value

Although the project includes artificial intelligence, AI was intentionally limited to the tasks where it provides measurable benefits.

AI is responsible for:

* Classifying incoming emails to distinguish procurement requests from advertisements or unrelated messages.
* Extracting procurement information from unstructured RFQs.
* Extracting supplier quotation data from replies that may have different layouts.

Incoming documents often include company logos, signatures, branding elements and unrelated information.

Instead of relying on rigid templates, AI identifies the procurement data that actually matters and converts it into a structured format ready for processing.

Business-critical operations are **not** delegated to AI.

Part matching, supplier tracking, RFQ state management, deadline handling, command parsing, validation and workflow decisions rely on deterministic logic implemented through custom JavaScript, regex processing and structured workflow design.

This approach combines AI flexibility with engineering reliability.

---

# Professional RFQ Generation

Generating an RFQ is much more than exporting data into Excel.

The generated document represents the company's professionalism.

For that reason, RFQ sheets are generated through dedicated Python services running inside Docker rather than simple spreadsheet exports.

Each RFQ is professionally formatted with:

* Company branding.
* Company logo.
* Organized layouts.
* Clear typography.
* Consistent styling.
* Highlighted supplier input fields.

Supplier-editable cells are intentionally colored to guide attention immediately toward the information suppliers are expected to provide.

This small visual decision reduces confusion, improves completion speed and creates a more professional experience for external suppliers.

Good document design strengthens business relationships.

---

# Human-Centered Supplier Selection

Sending RFQs to suppliers should be quick, reliable and resistant to mistakes.

Instead of requiring employees to type supplier names or email addresses manually, every supplier is assigned a unique internal Supplier ID.

Example:

send RFQ123 1,3,5 72h

The workflow automatically retrieves supplier information from the database and distributes the RFQ accordingly.

This design minimizes typing effort while significantly reducing the risk of sending quotations to incorrect recipients or forgetting important suppliers.

Sometimes a single typing mistake can mean losing the best quotation.

Small workflow decisions like this help prevent costly human errors.

---

# Transparent Procurement Tracking

One of the project's major goals was transparency.

Many automation systems hide operational data inside databases that only developers can inspect.

This project intentionally takes the opposite approach.

Google Sheets serves as both the operational database and a business-friendly inspection interface.

Managers and employees can immediately review:

* Current RFQ status.
* Pending quotations.
* Sent suppliers.
* Supplier responses.
* Extracted RFQ data.
* Matched and unmatched parts.
* Order history.
* Individual quotation data.

This visibility simplifies audits, debugging and day-to-day management without requiring technical knowledge.

---

# Intelligent Deadline Management

Waiting indefinitely for supplier replies slows procurement and affects customer satisfaction.

The platform therefore evaluates procurement completion using two independent conditions.

If every selected supplier replies before the deadline, the comparison process starts immediately.

Otherwise, a dedicated monitoring workflow checks deadlines every 30 minutes.

When the deadline expires, the comparison sheet is generated using every quotation received so far.

This prevents procurement from stalling because of one delayed supplier while maintaining predictable delivery times for customers.

---

# Executive-Ready Comparison Sheets

The comparison sheet was designed with two audiences in mind.

The engineer performing the technical evaluation.

The manager reviewing multiple procurement decisions.

Instead of immediately presenting detailed supplier data, the sheet begins with a concise summary containing key procurement information.

Managers can quickly understand the order without inspecting every individual quotation.

Below the summary, every supplier is displayed side-by-side with:

* Available quantity.
* Unit price.
* Net price.
* Delivery time.
* Remarks.

Keeping every quotation aligned horizontally allows engineers to compare suppliers naturally without switching between documents or manually organizing information.

The result is faster decision making with significantly less manual effort.

---

# Engineering Decisions

Several architectural decisions were made specifically to balance flexibility, reliability and usability.

### Google Sheets

Chosen because business users need complete visibility into procurement operations, not because it was the easiest database.

### n8n

Selected for orchestrating multiple services while still allowing extensive custom JavaScript whenever business logic required deterministic behavior.

### Python Services

Responsible for generating professionally designed Excel documents that standard spreadsheet nodes cannot produce.

### Docker

Used to isolate services, simplify deployment and keep every component independently maintainable.

### AI

Limited to extraction and classification while deterministic workflow logic remains responsible for operational decisions.

---

# Technical Overview

* More than 110 workflow nodes.
* Approximately 25% implemented as custom JavaScript code nodes.
* Three dedicated workflows.
* Dockerized deployment.
* Ubuntu VPS hosting.
* Python document generation services.
* Gmail integration.
* Telegram integration.
* Google Sheets operational database.
* OpenRouter-powered AI extraction.

The size of the workflow reflects the number of business scenarios handled rather than unnecessary complexity.

---

# Future Development

The current implementation intentionally focuses on solving real procurement problems instead of accumulating features.

Future improvements should always be driven by operational requirements gathered from businesses using the platform.

Every component of the architecture has been designed to remain adaptable so that procurement rules, communication platforms and workflow logic can evolve according to business needs.

---

# Disclaimer

This repository documents the architecture, engineering decisions and business capabilities of the system.

The workflow source code and workflow JSON files are intentionally excluded to protect the implementation while demonstrating the complete system design and functionality.
