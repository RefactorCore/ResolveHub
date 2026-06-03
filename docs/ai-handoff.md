# ResolveHub AI Handoff Prompt

You are continuing development of an existing project called ResolveHub.

IMPORTANT:
Do not assume anything.
Do not rewrite existing functionality unless necessary.
Do not create duplicate files.
Analyze the project first.

## Step 1 - Read Documentation

Review all files under:

/docs

Including:

* project-spec.md
* architecture.md
* api-contracts.md
* progress.md
* ai-handoff.md

Treat these files as the source of truth.

---

## Step 2 - Analyze Repository

Review the entire codebase.

Provide a summary of:

### Architecture

* Frontend structure
* Backend structure
* Storage approach
* Authentication approach
* API integrations

### Current Features

List completed functionality.

### Missing Features

List unfinished functionality.

### Technical Debt

List any concerns or recommendations.

Do not write code yet.

---

## Step 3 - Validate Against Specification

Compare the current implementation against project-spec.md.

Create a checklist:

* Completed
* Partial
* Missing

For every feature.

---

## Step 4 - Recommend Next Tasks

Provide:

1. Highest Priority Task
2. Quick Win Task
3. Technical Debt Task

Explain why.

---

## Project Overview

ResolveHub is an internal customer operations platform.

Purpose:

Track customer issues such as:

* Order Not Received
* Shipping Delay
* Wrong Address
* Damaged Item
* Missing Item
* Wrong Item
* Reship Request
* Refund Request
* Other

---

## Technology Stack

Frontend:

* HTML
* Tailwind CSS
* Vanilla JavaScript

Backend:

* Node.js
* Express.js

Storage:

* JSON Files

No:

* PostgreSQL
* MySQL
* MongoDB
* Firebase
* Supabase

---

## Authentication

Roles:

* Admin
* Agent

Users stored in:

/data/users.json

Authentication:

* JWT
* bcrypt

---

## Data Storage

Active Cases:

/data/cases

Archived Cases:

/data/archive

Uploads:

/uploads

---

## Service Points Integration

Environment Variables:

SERVICE_POINTS_API_KEY=
SERVICE_POINTS_BASE_URL=

Service File:

/services/servicepoints.js

Functions:

getOrder(orderNumber)

getTracking(orderNumber)

Service Points integration must remain isolated from business logic.

---

## Archive Requirements

Closed cases older than 90 days:

Move from:

/data/cases

To:

/data/archive

Requirements:

* Preserve notes
* Preserve attachments
* Preserve activity history
* Remain searchable
* Allow admin restore

---

## Development Rules

1. Preserve existing architecture.
2. Do not introduce paid services.
3. Do not introduce databases.
4. Use JSON storage only.
5. Keep code modular.
6. Follow existing coding style.
7. Update progress.md after major changes.
8. Explain changes before generating code.
9. Generate production-ready code.
10. Prefer small focused commits.

---

## Before Writing Code

Always answer:

1. What exists now?
2. What is missing?
3. What will you build next?
4. Which files will be modified?

Wait for approval before making major changes.
