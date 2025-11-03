# 🤖 AI Finance-Ops Agent: Bank-to-GL Reconciliation

This project demonstrates an **AI-assisted finance operations workflow** that automates the reconciliation between bank transactions and the General Ledger (GL).  
It was designed and built by **Marjaana Peeters**, AI-savvy finance professional, to explore how no-code agents and synthetic finance data can automate repetitive accounting processes.

---

## 🚀 Overview

**Purpose:**  
Automate the Bank → GL reconciliation process, including:
- Categorisation of bank lines  
- Matching to AR/AP invoices  
- Generating journal suggestions for unmatched lines  
- Maintaining a run log  
- Updating a live KPI dashboard (Google Sheets)

**Stack:**
- 🧠 ChatGPT / OpenAI Agent Builder (no-code visual canvas)
- 📊 Google Sheets & Drive for inputs / control / dashboard
- 🧾 CSV data store for synthetic finance transactions
- 🛠️ Optional integrations: Slack (alerts), Notion (reporting), n8n / Make (automation)
- 🐍 Python SDK (optional extension for dataset or API logic)

---

## 🗂️ Repository Structure
# 🤖 AI Finance-Ops Agent: Bank-to-GL Reconciliation

This project demonstrates an **AI-assisted finance operations workflow** that automates the reconciliation between bank transactions and the General Ledger (GL).  
It was designed and built by **Marjaana Peeters**, aspiring AI-savvy fractional CFO, to explore how no-code agents and synthetic finance data can automate repetitive accounting processes.

---

## 🚀 Overview

**Purpose:**  
Automate the Bank → GL reconciliation process, including:
- Categorisation of bank lines  
- Matching to AR/AP invoices  
- Generating journal suggestions for unmatched lines  
- Maintaining a run log  
- Updating a live KPI dashboard (Google Sheets)

**Stack:**
- 🧠 ChatGPT / OpenAI Agent Builder (no-code visual canvas)
- 📊 Google Sheets & Drive for inputs / control / dashboard
- 🧾 CSV data store for synthetic finance transactions
- 🛠️ Optional integrations: Slack (alerts), Notion (reporting), n8n / Make (automation)
- 🐍 Python SDK (optional extension for dataset or API logic)

---

## 🗂️ Repository Structure

Finance-Agent-Lab/
├── Templates/
│ └── Bank-to-GL_Reconciliation_Template/
│ ├── inputs_template/
│ │ ├── bank_transactions_template.csv
│ │ ├── ar_invoices_template.csv
│ │ ├── ap_bills_template.csv
│ │ └── gl_journal_template.csv
│ ├── Bank_Recon_Control_Template.xlsx
│ └── Bank_Recon_Output_Template.xlsx
├── README.md
└── docs/
├── screenshots/
└── finance-agent-architecture.png


---

## 📋 Workflow Steps

### 1️⃣ Inputs
Four CSVs act as input datasets (synthetic or real):
- `bank_transactions_template.csv`
- `ar_invoices_template.csv`
- `ap_bills_template.csv`
- `gl_journal_template.csv`

### 2️⃣ Control Sheet
Holds configuration, categorisation rules, and run log:
- `CONFIG`: file paths, tolerances  
- `CATEGORIES`: keyword → account mapping  
- `RUN_LOG`: timestamped record of each run

### 3️⃣ Output Sheet
Contains:
- `SUMMARY`  
- `MATCHED_AR` / `MATCHED_AP`  
- `UNMATCHED`  
- `SUGGESTED_JOURNALS`  
- `DASHBOARD` (live KPI & chart)

### 4️⃣ AI Agent
The OpenAI no-code Agent performs:
1. Load CSVs (from Google Drive)
2. Match AR/AP vs. bank data  
3. Categorise unmatched lines  
4. Generate journal suggestions  
5. Append run logs  
6. Refresh dashboard

### 5️⃣ Automation (optional)
- Slack alert if match rate < 95 %  
- n8n / Make flow to duplicate template folders for each client (`<PROJECT_NAME>`)  
- GitHub Actions / cron for nightly refresh

---

## 🧾 Example Outputs

| Metric | Value |
|---------|-------|
| Latest Run | 2025-10-13 13:15 |
| Bank Rows | 707 |
| Matched AP | 641 |
| Unmatched | 66 |
| Match Rate | 90.7 % |
| Comment | auto-cat + journals added |

**Suggested Journal Example**
| Date | Account | Memo | Debit | Credit |
|------|----------|------|--------|--------|
| 2025-01-12 | 5100 | Bank charges | 15.00 | 0.00 |
| 2025-01-12 | 1000 | Bank account | 0.00 | 15.00 |

---


🧩 Next Steps / Extensions
Add OCR invoice ingestion (Google Vision / Tesseract)
Integrate Slack/Teams for daily alerts
Link with QuickBooks or Xero API for posting journals
Build an n8n scenario for one-click monthly close

🧠 Author
Marjaana Peeters
AI-native strategic finance professional
LinkedIn: www.linkedin.com/in/marjaana-peeters-0442a4

🪪 License
MIT License – feel free to reuse, credit, and extend.


---

