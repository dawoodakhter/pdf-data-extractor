 📧 PDF Email Intake Agent

An intelligent n8n automation workflow that monitors a Gmail inbox for incoming emails with PDF attachments, extracts structured data using Google Gemini AI, and automatically logs results to Google Sheets — fully hands-free.

---

## 🚨 The Problem

Businesses receive important documents (invoices, contracts, reports) as PDF email attachments daily. Manually opening each email, reading the PDF, and copying data into a spreadsheet is:
- Time-consuming and repetitive
- Prone to human error
- Not scalable

---

## ✅ The Solution

This workflow automates the entire process end-to-end — from email detection to structured data logging — with zero manual intervention required.

---

## ⚙️ How It Works

```
Gmail Inbox
    │
    ▼
📨 Gmail Trigger (watches for emails with PDF attachments)
    │
    ▼
📄 Extract PDF Content (reads binary attachment)
    │
    ▼
🤖 Google Gemini AI (extracts structured data via prompt)
    │
    ▼
📊 Google Sheets (logs parsed fields automatically)
```

### Step-by-step:
1. **Gmail Trigger** — monitors inbox using `has:attachment filename:pdf` filter
2. **Extract from File** — reads the PDF binary attachment (`attachment_0`)
3. **Gemini AI Node** — prompt-engineered to return consistent JSON with key fields
4. **Google Sheets** — maps extracted JSON fields to spreadsheet columns automatically

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| [n8n](https://n8n.io) | Workflow automation platform |
| Gmail API | Email monitoring & attachment extraction |
| Google Gemini API | AI-powered PDF data extraction |
| Google Sheets API | Structured data logging |

---

## 📋 Prerequisites

- n8n Cloud account (or self-hosted n8n)
- Google account with Gmail and Sheets access
- Google Gemini API key
- OAuth2 credentials configured in n8n for Gmail and Google Sheets

---

## 🚀 Setup

1. **Clone or import** the workflow JSON into your n8n instance
2. **Configure credentials:**
   - Add Gmail OAuth2 credential in n8n
   - Add Google Sheets OAuth2 credential in n8n
   - Add Gemini API key credential in n8n
3. **Update the Gmail Trigger** search filter if needed (`has:attachment filename:pdf`)
4. **Update the Google Sheets node** with your target Spreadsheet ID and Sheet name
5. **Customize the Gemini prompt** to match the fields you want to extract from your PDFs
6. **Publish** the workflow in n8n Cloud to activate it

---

## 📁 Project Structure

```
pdf-email-intake-agent/
├── workflow.json          # n8n workflow export
├── README.md              # This file
└── sample-output.png      # Example Google Sheets output (optional)
```

---

## 💡 Use Cases

- Invoice processing & accounts payable automation
- Contract data extraction
- Resume/CV parsing from email applications
- Report intake and logging systems

---

## 👤 Author

**Daud** — AI Automation Engineer  
[LinkedIn](https://linkedin.com/in/your-profile) • [GitHub](https://github.com/your-username)

---

## 📄 License

MIT License — feel free to use and adapt this workflow for your own projects.
