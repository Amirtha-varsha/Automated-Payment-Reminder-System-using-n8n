# Automated Payment Reminder System using n8n

## Project Overview
This project is an automated payment reminder system built using n8n, Google Sheets, and Twilio WhatsApp/SMS API. It automatically checks payment records daily and sends appropriate messages based on payment status.Each case triggers a different personalized message.The workflow identifies three cases:
* ⚠️ Payment Due Today (Pending)
* ⏰ Payment Overdue (Pending)
* ❤️ Payment Completed Today

---

## Key Features

- Fully automated daily execution
- Reads live data from Google Sheets
- Intelligent classification of payment status
- Multi-condition decision logic
- WhatsApp/SMS notifications via Twilio
- Appreciation messages for completed payments
- Production-style workflow design

---

## Workflow Architecture
**Schedule Trigger → Google Sheets (Fetch Data) → Set Node (Today's Date) → Python Code Node (Classification) → IF Node (Decision Logic)  → Twilio WhatsApp/SMS**

 ---
 
## Decision Logic

The system classifies each record into:
Type	Condition
* 📅 due_today	Status = pending AND due date = today
* ⚠️ overdue	Status = pending AND overdue date = today
* ❤️ completed	Status = done AND due date = today

---

## Tech Stack

n8n — Workflow Automation Platform

Google Sheets API — Data source

Twilio API — WhatsApp/SMS messaging

Python (n8n Code Node) — Data processing

## Dataset Structure
| Name   | Email                                     | number     | Due date   | Status   | Overdue Date   |
| ------ | ----------------------------------------- | -----------| ---------- | -------- | -------------- |
| User A | [usera@email.com](mailto:usera@email.com) | xxxxxxxxxx | 27-02-2026 | Pending  | 28-02-2026     |
| User B | [userb@email.com](mailto:userb@email.com) | xxxxxxxxxx | 28-02-2026 | complete | 01-03-2026     |

Date format used: DD-MM-YYYY

---
## Use Cases

* Fee reminders for institutions
* Subscription renewals
* Loan EMI notifications
* Utility bill reminders
* Customer follow-up automation
---
## What I Learned

* Designing real-world automation workflows
* Conditional branching logic
* API integration (Twilio)
* Data processing in low-code platforms
* Error handling and debugging in automation
