# 🧪 n8n Test Case Generator Workflow

This project contains an [n8n](https://n8n.io) automation workflow that reads requirements from a Google Sheet, sends the requirement to OpenAI for test case generation, and writes the test cases back to another Google Sheet.

---

## 🚀 Workflow Overview

- **Reads** requirements from Google Sheet (e.g. login functionality).
- Sends prompts to **OpenAI GPT-3.5** to generate test cases.
- **Parses** and extracts just the test cases from the response.
- **Appends** the generated test cases to another Google Sheet with fields like:
  - ID
  - Feature
  - Requirement
  - Priority
  - Test Cases
  - Remarks

---

## 📁 Files in This Repo

- `generate-testcases-workflow.json` – The exported n8n workflow file
- `Output Testcases.xlsx` – (Sheet1:Requirement, Sheet2: generated testcases)
- `README.md` – This file with documentation

---

## ✅ How to Use

1. Import the `.json` workflow into your n8n instance.
2. Set up credentials for Google Sheets and OpenAI in n8n.
3. Modify Google Sheet IDs and ranges in the workflow nodes.
4. Run the workflow manually or schedule it using a Cron node.

---

## 📌 Requirements

- n8n (Self-hosted or cloud)
- OpenAI API key
- Google Sheets API credentials
