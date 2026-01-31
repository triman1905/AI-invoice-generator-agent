# Automated Invoice Generator & Email Sender (n8n)

An automated invoicing system built using n8n, Google Sheets, HTTP APIs, JavaScript, and Gmail.  
This workflow generates invoices, sends them as email attachments, and updates invoice status automatically.

---

## Project Overview

This project automates the entire invoice lifecycle:
- Reads invoice data from Google Sheets
- Generates professional invoices dynamically
- Sends invoices via email
- Updates invoice status after sending

It is ideal for freelancers, agencies, and small businesses.

---

## Workflow Breakdown

### Trigger
- Workflow starts when "Execute workflow" is clicked.
- Can be scheduled using a Cron trigger for monthly billing.

### Get Rows from Google Sheets
- Reads invoice details such as:
  - Client name
  - Email
  - Invoice number
  - Amount
  - Due date
  - Status

### Loop Over Items
- Processes invoices one-by-one.
- Ensures accurate status updates.

### Template Rendering
- Generates invoice layout dynamically.
- Injects client and billing details into the template.

### HTTP Request
- Sends invoice data to an API or service.
- Generates a downloadable PDF invoice.

### JavaScript Code Node
- Formats email subject and body.
- Attaches the generated invoice PDF.

### Send Email via Gmail
- Sends a professional invoice email with PDF attachment.

### Update Row in Google Sheets
- Updates invoice status (SENT / UNREAD).
- Logs timestamp for record keeping.

---

## Invoice Details

- Client information
- Invoice number
- Invoice date and due date
- Service description
- Tax calculation
- Total payable amount

---

## Tech Stack

- n8n
- Google Sheets API
- Gmail API
- HTTP API
- JavaScript

---

## Key Features

- Automated invoice generation
- PDF invoice creation
- Email delivery with attachments
- Status tracking in Google Sheets
- Minimal manual effort

---

## Use Cases

- Freelancer billing
- Monthly retainers
- Agency invoicing
- Subscription services

---

## Author

Triman Kaur  
Web Developer | Automation & AI Enthusiast
