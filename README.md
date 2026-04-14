# 🏦 Automated Employee Payroll Direct Deposit Request System

Built with **n8n** | Google Sheets | Gmail | Webhooks

---

## 📋 The Problem

In many companies, employees who want to update their payroll direct deposit details
have to email HR manually. This creates problems:

- Requests get lost in inboxes
- No tracking or audit trail
- HR has to manually verify employee identity
- No structured approval process
- Employees don't know the status of their request

---

## ✅ The Solution

A fully automated end-to-end request and approval system built in n8n that handles
everything from submission to approval — with zero manual steps for HR.

---

## ⚙️ How It Works

### Employee Side
1. Employee fills out a form with their name, ID, bank details and email
2. System generates a unique Request ID automatically
3. Employee ID is validated against the company employee database (Google Sheets)
4. If invalid → employee receives an email asking them to reconfirm their details
5. If a pending request already exists → employee is notified automatically
6. If valid and new → request is logged and HR is notified for approval

### HR Side
1. HR receives an email with one-click Approve or Reject buttons
2. Clicking a button triggers the approval webhook
3. System checks the request is still pending (prevents double-processing)
4. If approved → employee record is updated + employee receives approval email
5. If rejected → request is logged + employee receives rejection email

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| n8n | Workflow automation |
| Google Sheets | Employee database & request tracking |
| Gmail | Employee & HR email notifications |
| n8n Webhooks | HR approval/rejection trigger |
| n8n Forms | Employee submission form |

---

## 💡 Key Features

- **Employee ID validation** before any request is processed
- **Duplicate request detection** — prevents the same employee submitting twice
- **Unique Request ID** generated for every submission
- **Full audit log** — every action is tracked in Google Sheets
- **Double-processing protection** — HR can't approve/reject the same request twice
- **Automated emails** at every stage for both employee and HR

---

## 📁 Files

- `workflow.json` — The n8n workflow (import directly into your n8n instance)

---

## 🚀 How To Use This Workflow

1. Download `workflow.json`
2. Open your n8n instance
3. Click **Import** and select the file
4. Connect your own Google Sheets and Gmail credentials
5. Update the Google Sheet IDs to point to your own sheets
6. Activate the workflow

---

*Built by [Martins](https://github.com/martinsautomates) as part of an n8n automation portfolio*
