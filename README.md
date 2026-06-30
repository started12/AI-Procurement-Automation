# 🚀 AI Procurement Automation

> **An engineering-driven procurement automation platform that streamlines the complete procurement lifecycle using intelligent document processing, deterministic business logic, and professional document generation.**

---

## 📖 Overview

Procurement is one of the most repetitive and detail-sensitive operations inside engineering, manufacturing, and industrial companies. A single Request for Quotation (RFQ) usually starts a long chain of manual tasks: reading emails, extracting dozens of part numbers, creating spreadsheets, contacting suppliers, tracking replies, comparing quotations, and finally preparing information for engineering or management to make purchasing decisions.

Although each individual task appears simple, together they consume a significant amount of engineering time while introducing unnecessary opportunities for human error.

This project was built to eliminate those repetitive operations without sacrificing reliability, transparency, or professionalism.

Rather than automating isolated actions, the platform automates the **entire procurement lifecycle**, beginning with an incoming RFQ and ending with a professionally generated quotation comparison sheet ready for engineering review.

The workflow combines AI where flexibility is required, deterministic business logic where reliability is critical, and carefully designed document generation to ensure every interaction reflects the company's professional image.

Unlike many automation projects that demonstrate technical integrations, this system was designed around **real procurement practices**, using real RFQ structures and real operational workflows to ensure that every engineering decision solves an actual business problem.

---

# 🎯 Why This Project Exists

Every procurement department shares the same challenge.

Employees spend a large portion of their working hours performing repetitive administrative tasks that add very little business value.

Typical procurement activities include:

- Reading incoming RFQ emails.
- Extracting part numbers manually.
- Creating quotation sheets from scratch.
- Searching company databases for matching parts.
- Contacting suppliers individually.
- Waiting for supplier replies.
- Continuously checking inboxes for new quotations.
- Remembering which suppliers have replied.
- Following up with suppliers who missed deadlines.
- Creating quotation comparison sheets manually.
- Organizing information for engineering and management.

Most of these tasks require attention rather than engineering expertise.

The result is lost productivity, inconsistent documentation, unnecessary delays, and increased opportunities for human mistakes.

This platform was designed to remove those repetitive operations while keeping employees fully informed and maintaining complete visibility over every procurement order.

The objective was never to build an "AI workflow."

The objective was to build a procurement solution that engineers would actually enjoy using.

---

# 💡 Design Philosophy

Throughout development, one principle guided every engineering decision:

> **Every component of the system exists because it solves a real business problem.**

Features were never added simply because they looked impressive.

Every workflow, every database table, every notification, every generated document, every code node, and every design decision exists to improve at least one of the following:

- Reduce manual work.
- Reduce human mistakes.
- Improve business reliability.
- Save engineering time.
- Improve supplier experience.
- Improve manager visibility.
- Produce more professional outputs.

Whenever technical complexity conflicted with business usability, business usability always came first.

The system is intentionally designed to adapt to business requirements—not the other way around.

---

# 🏗️ System Architecture

> 📷 **Architecture Diagram Placeholder**

*(A complete system architecture diagram will be inserted here.)*

The platform follows a complete procurement lifecycle rather than automating isolated tasks.

```text
Incoming RFQ
      │
      ▼
Document Classification
      │
      ▼
AI Data Extraction
      │
      ▼
Part Matching
      │
      ▼
Order Registration
      │
      ▼
Telegram Notification
      │
      ▼
Supplier Selection
      │
      ▼
Professional RFQ Generation
      │
      ▼
Supplier Distribution
      │
      ▼
Supplier Response Tracking
      │
      ▼
Deadline Monitoring
      │
      ▼
Comparison Sheet Generation
      │
      ▼
Engineering Decision
```

Every stage has a clearly defined responsibility, allowing the system to remain modular, traceable, and easy to expand as business requirements evolve.

---

# ✨ Business Capabilities

Rather than thinking of the project as "an automation workflow", it is better described as a procurement platform composed of several business capabilities working together.

Each capability was designed to solve a specific operational problem.

---

## 📥 Multi-Format RFQ Processing

Companies rarely receive procurement requests in a single standardized format.

Some customers send Excel sheets.

Others attach PDFs.

Some simply write their requirements directly inside an email.

Many even send screenshots or images containing part numbers that cannot be copied into spreadsheets.

Instead of forcing employees to manually rewrite every request into a usable format, the platform accepts multiple input formats including:

- Excel (.xlsx)
- PDF
- Plain Text
- Images

Supporting image-based RFQs is particularly valuable.

Without automated extraction, procurement employees often spend several minutes manually typing every part number, description, and requested quantity before any procurement work can even begin.

This repetitive work provides no business value while increasing the possibility of typing mistakes.

By supporting multiple document formats from the beginning, the workflow adapts to the client's preferred communication method instead of forcing clients to adapt to the system.

---

## 🧩 Intelligent Part Matching

Once procurement data has been extracted, every requested part is validated against the company's internal parts database.

The matching process immediately separates:

- Successfully matched parts.
- Unknown parts.
- Missing parts.

Instead of discovering missing inventory later during procurement, employees are informed immediately.

This early validation provides multiple benefits:

- Faster procurement decisions.
- Immediate visibility into unavailable inventory.
- Reduced manual database searching.
- Better preparation before contacting suppliers.

Employees also receive a clear summary showing matched and unmatched items, allowing them to investigate potential data issues before procurement continues.

---

## 📦 Procurement State Management

Procurement is not a single action.

It is a lifecycle.

One of the most important engineering challenges solved by this project was tracking the current state of every RFQ from beginning to end.

Instead of treating procurement requests as independent emails, each RFQ moves through a well-defined lifecycle.

Typical states include:

- Pending Supplier Selection
- RFQs Sent
- Waiting for Supplier Responses
- Partially Responded
- Comparison Generated
- Quoted
- Cancelled

Maintaining these states provides complete visibility over every procurement request.

At any moment, employees and managers can immediately determine:

- Which RFQs require action.
- Which suppliers have already responded.
- Which quotations are still pending.
- Which comparisons have already been completed.

This structured lifecycle removes uncertainty while making procurement significantly easier to monitor.

---

## 📨 Automated Supplier Communication

Once suppliers have been selected, the workflow automatically generates and distributes professionally formatted RFQ sheets.

Employees no longer need to:

- Create spreadsheets manually.
- Copy procurement data repeatedly.
- Write multiple supplier emails.
- Attach quotation sheets individually.
- Keep track of who received which RFQ.

Every supplier receives:

- A professionally designed RFQ sheet.
- Company branding.
- Clear supplier instructions.
- A predefined response deadline.

Automating supplier communication not only saves engineering time but also ensures every supplier receives consistent documentation, reducing misunderstandings and improving the company's professional image.

---

## 🔍 Complete Traceability

Every procurement event is recorded.

Nothing disappears once the workflow finishes.

Throughout the lifecycle, the platform maintains traceability for:

- RFQ IDs
- Client information
- Order details
- Individual order lines
- Selected suppliers
- Supplier responses
- Response deadlines
- Generated RFQs
- Generated comparison sheets
- Current procurement status

Rather than becoming a "black box", the workflow creates a complete history that can later be reviewed for auditing, troubleshooting, management review, or operational analysis.

This visibility was one of the primary design goals of the platform and influenced many architectural decisions discussed later in this documentation.

# 🧠 AI Where It Matters, Logic Where It Counts

Artificial Intelligence is an important component of this platform—but it is intentionally **not** the center of it.

One lesson learned throughout development was that giving AI too much control over business operations reduces reliability instead of improving it.

For that reason, AI is only responsible for tasks where flexibility is genuinely valuable, while every business-critical decision is handled using deterministic logic, custom JavaScript, regular expressions, and structured workflow design.

This balance allows the platform to benefit from AI without sacrificing consistency or operational trust.

---

## 🤖 Intelligent RFQ Classification

Every incoming email is inspected before the procurement workflow begins.

Not every email arriving in a procurement mailbox deserves processing.

Advertisements, newsletters, promotional campaigns, and unrelated conversations would waste computing resources, create unnecessary notifications, and potentially generate invalid procurement orders.

To prevent this, AI performs an initial classification step.

Each incoming email is categorized as either:

- Valid Procurement Inquiry
- Supplier Response
- Ignore

This simple decision dramatically improves system reliability by ensuring that only relevant procurement activities continue through the workflow.

Instead of automating everything, the platform first decides **whether automation should happen at all**.

---

## 📑 Intelligent Data Extraction

Once a document has been classified, AI extracts only the information required for procurement.

Incoming RFQs and supplier quotations rarely follow identical templates.

Different companies organize their documents differently.

Some include logos, signatures, marketing content, company addresses, legal text, or other information that provides no procurement value.

Instead of depending on rigid templates, AI isolates only the data that matters.

Typical extracted information includes:

- Part Number
- Description
- Requested Quantity
- Available Quantity
- Unit Price
- Net Price
- Delivery Time
- Currency
- Warehouse
- Supplier Remarks

The extracted information is then converted into a structured format that the rest of the workflow can process consistently regardless of the original document layout.

This significantly increases compatibility with different suppliers and customers while reducing manual data entry.

---

## ⚙️ Deterministic Business Logic

Once procurement data becomes structured, AI steps aside.

From this point onward, the workflow relies on deterministic engineering rather than probabilistic reasoning.

Business operations including:

- Part matching
- RFQ ID generation
- Supplier selection
- Status tracking
- Deadline calculations
- Database updates
- Response tracking
- Comparison generation
- Telegram command parsing
- Regular expression processing
- Data validation

are all handled through workflow logic and custom JavaScript.

This approach ensures predictable behaviour every single time.

The goal is not to replace engineering with AI.

The goal is to combine the strengths of both.

---

# 📋 Professional RFQ Generation

An RFQ is often the first document a supplier receives from a company.

For many suppliers, it creates the first impression of how organized and professional the company is.

For that reason, generating quotation sheets became far more than simply exporting information into Excel.

Instead of relying on basic spreadsheet nodes, this platform uses dedicated Python services running inside Docker containers to generate professionally designed Excel documents.

Each generated RFQ includes:

- Company branding
- Company logo
- Organized layout
- Consistent typography
- Structured procurement information
- Clearly separated sections
- Highlighted supplier input fields

Special attention was given to supplier usability.

The cells suppliers are expected to complete are intentionally highlighted using distinctive colours, allowing suppliers to immediately recognize where their information should be entered.

Although this may appear to be a small visual improvement, it reduces confusion, speeds up quotation completion, and demonstrates professionalism.

Good document design strengthens supplier relationships.

Every generated RFQ should look like it was prepared carefully by the company—not automatically generated by software.

---

# 💬 Telegram Command Center

One of the primary objectives of the platform was minimizing employee interaction while keeping complete operational control.

Instead of requiring employees to navigate multiple dashboards or web interfaces, the system can be controlled entirely from Telegram.

Telegram was selected because of its reliable API, fast communication, generous file sharing capabilities, and support for long messages and document attachments without the limitations found on many messaging platforms.

The objective was simple:

**Allow procurement employees to complete their daily work without leaving their communication platform.**

---

## 📤 Sending RFQs

Once a new procurement request has been reviewed, the employee simply specifies:

- Which RFQ should be processed.
- Which suppliers should receive it.
- How long suppliers have to respond.

Example:

```text
send RFQ_ABC123 1,3,5 72h
```

or

```text
send RFQ_ABC123 1,3,5 3d
```

Instead of typing supplier names or email addresses manually, employees simply provide Supplier IDs.

The workflow automatically retrieves supplier information from the database before distributing professionally generated RFQ sheets.

Supporting both **72h** and **3d** was a deliberate engineering decision.

Different employees naturally express deadlines differently.

Rather than forcing users to memorize one specific syntax, the workflow understands both formats automatically.

Good software adapts to its users—not the opposite.

---

## 📋 Pending Orders

```text
list pending
```

Displays every RFQ currently waiting for supplier selection.

Employees immediately know which procurement requests still require action without searching through emails or spreadsheets.

This greatly reduces the chance of forgetting newly received procurement inquiries during busy working days.

---

## 📑 Complete Procurement Overview

```text
list all
```

Returns every procurement order currently tracked by the platform together with its current lifecycle status.

Instead of opening multiple spreadsheets, employees receive a complete operational overview within seconds.

---

## 🔍 RFQ Status

```text
status RFQ_ABC123
```

Returns the complete lifecycle of a single RFQ.

Possible states include:

- Pending Supplier Selection
- Sent to Suppliers
- Waiting for Responses
- Partially Responded
- Comparison Generated
- Quoted
- Cancelled

This command removes uncertainty by allowing employees to instantly understand the current state of any procurement request.

---

## ❌ Cancelling Procurement

```text
cancel RFQ_ABC123
```

Cancels an existing procurement request whenever business priorities change.

Cancelled orders remain recorded instead of being deleted, preserving complete procurement history for future review and auditing.

---

# ⏳ Intelligent Deadline Processing

Following supplier responses manually is one of the most repetitive procurement activities.

Employees often find themselves refreshing inboxes throughout the day while trying to remember:

- Which suppliers have already replied.
- Which quotations are still missing.
- Whether enough responses have been received to begin evaluation.

This platform removes that responsibility entirely.

Every procurement request includes a response deadline chosen directly by the employee.

Whether entered as:

```text
72h
```

or

```text
3d
```

the workflow converts the value into an exact deadline and stores it for continuous monitoring.

The comparison process then follows two independent business rules.

### ✅ Rule One — Every Supplier Responded

Whenever a supplier submits a quotation, the workflow checks whether that supplier is the final outstanding response.

If every selected supplier has already replied, the comparison sheet is generated immediately.

There is no reason to delay procurement once all required quotations have been received.

---

### ⏰ Rule Two — Deadline Reached

Not every supplier responds on time.

Waiting indefinitely would delay procurement, postpone customer deliveries, and negatively affect business reliability.

To prevent this, a dedicated monitoring workflow executes every 30 minutes.

Its only responsibility is checking whether any procurement deadlines have expired.

If the deadline is reached before every supplier has responded, the platform automatically generates the comparison sheet using every quotation received so far.

Procurement continues without unnecessary delays while still giving suppliers a fair opportunity to participate.

This behaviour reflects real procurement operations rather than theoretical workflow automation.

---

# 📊 Transparent Data Management

Many automation platforms behave like black boxes.

Information flows through the workflow, but managers have very little visibility into what actually happened.

This project intentionally follows the opposite philosophy.

Google Sheets was selected not only as an operational database but also as a transparent management interface.

Every procurement event remains visible throughout the complete lifecycle.

Managers and employees can inspect:

- Current RFQ status
- Client information
- Extracted RFQ data
- Order details
- Individual order lines
- Selected suppliers
- Supplier response status
- Response deadlines
- Matched and unmatched parts
- Generated RFQs
- Supplier quotation data
- Final comparison data

Rather than depending on developers to inspect hidden databases, procurement teams can investigate orders themselves whenever questions arise.

This greatly simplifies daily management, internal auditing, troubleshooting, and operational reviews.

The platform stores information using several dedicated data structures, each with a clearly defined responsibility.

Examples include:

- Orders
- Order Lines
- Supplier Directory
- RFQ–Supplier Relationships
- Supplier Quote Data
- Client RFQ Sheets
- Comparison Data

Every structure remains connected using RFQ IDs and Supplier IDs, preserving complete traceability from the original client inquiry to the final supplier comparison.

The objective was never simply storing data.

The objective was making procurement transparent.

---

# 📈 Executive-Ready Comparison Sheets

Receiving supplier quotations is only half of the procurement process.

Engineering teams still need to compare every supplier before making purchasing decisions.

Manually copying supplier quotations into comparison spreadsheets is one of the most time-consuming procurement activities.

The platform completely automates this process.

Once procurement reaches completion, a professionally designed comparison sheet is generated automatically.

The document was intentionally designed for **two different audiences**.

### 👨‍💼 Managers

The beginning of the comparison sheet contains a concise executive summary including important procurement information such as RFQ details, quotation date, and supplier deadline.

Managers reviewing multiple procurement requests can quickly understand the order without analysing every supplier row individually.

---

### 👨‍🔧 Engineers

Below the summary, suppliers are displayed side-by-side.

Each supplier includes:

- Available Quantity
- Unit Price
- Net Price
- Delivery Time
- Remarks

Keeping every quotation aligned horizontally allows engineers to compare suppliers naturally without switching between multiple documents.

The comparison sheet is designed to reduce visual effort while accelerating engineering decisions.

Although a simple price recommendation can be generated, supplier selection ultimately depends on company-specific procurement rules.

For that reason, the platform intentionally leaves the final purchasing decision to engineering professionals instead of attempting to replace business judgement.

# 🏗️ Engineering Decisions

One of the primary goals during development was building a system that could be trusted in real business environments rather than simply demonstrating automation capabilities.

Every architectural decision was made by asking one question:

> **"Will this make procurement more reliable, more transparent, or easier for employees to use?"**

The answers to that question shaped every component of the platform.

---

## 🎯 Business Before Technology

Throughout the project, business requirements always took priority over technical preferences.

Whenever a feature, technology, or implementation detail conflicted with the way procurement teams naturally work, the implementation was changed—not the business process.

The workflow was designed around real procurement practices rather than forcing procurement departments to adapt to software limitations.

This philosophy influenced almost every engineering decision inside the project.

---

## 🧠 AI Assists, Logic Decides

Artificial Intelligence performs tasks where flexibility provides clear value.

Business decisions, however, should remain predictable.

For that reason, AI is responsible for:

- Document classification.
- RFQ extraction.
- Supplier quotation extraction.

Everything else is deterministic.

Business logic such as supplier tracking, procurement state management, deadline processing, RFQ generation, database updates, comparison generation, Telegram commands, validations, and regular expression parsing are handled through workflow logic and custom JavaScript.

This combination provides the flexibility of AI while preserving the reliability expected inside engineering departments.

---

## 📊 Visibility Over Complexity

Many automation systems hide everything behind APIs and databases.

While technically effective, they often reduce visibility for managers and procurement employees.

This platform intentionally favors transparency.

Instead of storing information where only developers can inspect it, procurement data remains visible inside structured Google Sheets that can be reviewed without technical knowledge.

Managers can inspect procurement progress themselves.

Employees can verify supplier responses.

Engineering teams can investigate procurement history.

The workflow never becomes a black box.

---

## 👥 Every User Was Considered

This project was not designed only for automation.

It was designed for the people interacting with the automation.

Every user experiences the system differently.

### Procurement Employees

- Fewer repetitive tasks.
- No repeated spreadsheet creation.
- No manual supplier tracking.
- Fast Telegram commands.
- Automatic comparison generation.

### Suppliers

- Professionally designed RFQs.
- Clearly highlighted editable fields.
- Consistent document formatting.
- Better readability.

### Engineering Teams

- Side-by-side supplier comparison.
- Organized quotation data.
- Less manual processing.
- Faster purchasing decisions.

### Managers

- Complete procurement visibility.
- Executive summaries.
- Easy inspection of every procurement stage.
- Full traceability without requesting technical assistance.

Small usability improvements often produce greater business value than adding another technical feature.

---

## 🧩 Modular Architecture

The platform was intentionally divided into independent workflows rather than building one large automation.

### Workflow One

Receives incoming emails.

- RFQ detection.
- Supplier response detection.
- Advertisement filtering.
- AI extraction.
- Part matching.
- Order registration.
- Employee notification.

---

### Workflow Two

Processes Telegram commands.

Responsible for:

- Sending RFQs.
- Checking procurement status.
- Listing pending orders.
- Listing all orders.
- Cancelling procurement requests.

Keeping employee interaction isolated makes future expansion significantly easier.

---

### Workflow Three

Runs continuously in the background.

Every thirty minutes it checks supplier deadlines.

Whenever an RFQ reaches its response deadline, procurement continues automatically without employee intervention.

Separating deadline management from the main workflow improves reliability while keeping every workflow focused on one responsibility.

---

# ⚙️ Technical Overview

Although the platform focuses primarily on business operations, several technologies work together behind the scenes.

### Core Platform

- n8n

---

### Artificial Intelligence

- OpenRouter

---

### Programming Languages

- JavaScript
- Python

---

### Infrastructure

- Docker
- Ubuntu VPS

---

### Integrations

- Gmail
- Telegram
- Google Sheets
- Excel Processing Services

---

### Internal Components

- AI Document Classification
- Multi-format Data Extraction
- RFQ Generator
- Comparison Sheet Generator
- Supplier Tracking
- Procurement State Management
- Deadline Monitoring
- Order Database
- Supplier Database
- Response Tracking

---

# 📂 Repository Structure

```text
AI-Procurement-Automation/

│
├── README.md
│
├── assets/
│   ├── architecture.png
│   ├── workflow-overview.png
│   ├── incoming-rfq.png
│   ├── telegram-notification.png
│   ├── supplier-command.png
│   ├── generated-rfq.png
│   ├── comparison-sheet.png
│   ├── database-structure.png
│   └── workflow-sections.png
│
├── docs/
│   ├── architecture.md
│   ├── workflows.md
│   ├── deployment.md
│   └── engineering-decisions.md
│
└── LICENSE
```

As additional documentation is created, this repository will continue to grow while keeping the project organized and easy to navigate.

---

# 🔮 Future Development

One lesson learned while building this platform is that procurement workflows are never identical between companies.

Every organization follows different approval chains, supplier relationships, purchasing policies, and engineering procedures.

Because of that, this project intentionally avoids adding features simply to increase complexity.

Future development should always be driven by operational requirements rather than assumptions.

The modular architecture allows organizations to customize nearly every stage of the workflow, including:

- Communication platforms.
- AI providers.
- Procurement rules.
- Supplier approval processes.
- Internal databases.
- ERP integrations.
- Notification systems.
- Document templates.
- Reporting workflows.

The platform is designed to adapt to business requirements—not to force businesses into predefined workflows.

---

# 📚 Lessons Learned

Developing this platform reinforced several engineering principles.

### Professional outputs matter.

Automation should not only save time.

It should also improve how a company presents itself internally and externally.

Professionally generated RFQs and comparison sheets become part of the company's image.

---

### AI is not always the answer.

Artificial Intelligence is extremely valuable for interpreting unstructured information.

However, deterministic business logic remains the most reliable solution for operational decision-making.

Choosing where **not** to use AI became just as important as deciding where to use it.

---

### Small details prevent expensive mistakes.

Many seemingly minor decisions significantly improve reliability.

Examples include:

- Supplier IDs instead of manually typing email addresses.
- Automatic deadline handling.
- Procurement state tracking.
- Complete RFQ traceability.
- Thread ID matching for supplier replies.
- Transparent operational databases.

Small improvements accumulate into a noticeably better user experience.

---

### Visibility builds trust.

Managers should never need developers to understand what is happening inside procurement.

Keeping procurement information transparent makes the platform easier to manage, easier to debug, and easier to trust.

---

# 📷 Demonstration

This repository documents the project using screenshots taken directly from the running system.

The following demonstrations will be included throughout the documentation:

- System Architecture
- Incoming RFQ
- Workflow Overview
- Telegram Notifications
- Telegram Commands
- Generated RFQ Sheet
- Supplier Response
- Comparison Sheet
- Google Sheets Database
- Order Tracking
- Deadline Processing

Each image is intended to explain one stage of the procurement lifecycle.

---

# 📄 Disclaimer

This repository documents the architecture, engineering decisions, workflows, and business capabilities of the project.

The workflow JSON files, Python source code, prompts, and implementation details are intentionally excluded.

The purpose of this repository is to demonstrate the engineering approach, system design, and operational capabilities while protecting the implementation itself.

---

# Thank You

Thank you for taking the time to explore this project.

Building this platform was far more than connecting APIs or automating repetitive tasks.

It was an opportunity to study a real procurement process, understand the daily challenges faced by procurement teams, and engineer a solution that improves reliability, transparency, and efficiency without sacrificing the human experience.

Whether you're an engineer, recruiter, automation specialist, or business owner, I hope this documentation clearly demonstrates not only what the platform does, but why every design decision was made.

If you have feedback, ideas, or would like to discuss procurement automation, feel free to reach out.

Phone Number : +201066338302
