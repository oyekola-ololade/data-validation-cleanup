# CSV Data Validation & Cleanup

Validates email, phone, and date fields row-by-row and exports only clean, normalized contacts to the CRM.

![n8n](https://img.shields.io/badge/-n8n-333?style=flat-square) ![CRM HTTP API](https://img.shields.io/badge/-CRM%20HTTP%20API-333?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-workflow-EA4B71?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

**[Open the visual project page →](./index.html)**

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Workflow](#workflow)
- [Tech Stack](#tech-stack)
- [Demo status](#demo-status)
- [Setup](#setup)
- [Repository Structure](#repository-structure)
- [Disclaimer](#disclaimer)

## Overview

**Trigger:** Webhook (CSV upload: rows)

Validates email, phone, and date fields row-by-row and exports only clean, normalized contacts to the CRM.

### Key Features

- Field-level validation (email, phone, date)
- Automatic data normalization
- Separate error-report export for manual fixes

## Architecture

Open the [visual project page](./index.html#architecture) for the flow derived from the sanitized export.


## Workflow

1. CSV upload webhook receives the row data
2. Validate email format, phone format, and date validity per row
3. Valid rows: normalize email/phone casing and title-case the name, then export to the CRM
4. Invalid rows: log the row and its specific validation errors
5. Export the error report separately for manual review

## Tech Stack

- n8n
- CRM HTTP API

## Demo status

A configured live-run recording is not included yet. Credentials and service identifiers remain placeholders.


## Setup

1. Import `workflow/T25_Data_Validation_Cleanup.json` into your n8n instance (**Workflows → Import from File**).
2. Replace every placeholder credential/URL in the workflow (e.g. `YOUR_..._API_KEY`, `YOUR_..._URL`) with your own service credentials.
3. Activate the workflow and point the relevant integration (webhook source, scheduled trigger, etc.) at the generated webhook URL.
4. Test with a sample payload before going live.

## Repository Structure

```text
.
├── index.html
├── README.md
├── LICENSE
├── .gitignore
└── workflow/
    └── T25_Data_Validation_Cleanup.json
```


## Disclaimer

This workflow was built as a portfolio/template project to demonstrate n8n workflow automation and AI integration. API credentials and sensitive configuration have been removed before publication — replace all `YOUR_..._KEY` / `YOUR_..._URL` placeholders with your own before use.

---

Designed and engineered by

**Oyekola Ololade**

AI Systems & Integration Engineer

- LinkedIn: <http://linkedin.com/in/ololade-oyekola-5b1797397>
- Email: <oyekolaololade69@gmail.com>
