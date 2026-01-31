# AI-invoice-generator-agent

🧾 Automated Invoice Generator & Email Sender (n8n)

This project is an end-to-end invoice automation system built using n8n, Google Sheets, HTTP APIs, JavaScript, and Gmail.
It automatically generates invoices, sends them via email as attachments, and updates the invoice status back into Google Sheets.

Perfect for freelancers, startups, agencies, or SaaS billing workflows.

🚀 Project Overview

The workflow reads invoice data from Google Sheets, dynamically generates a professional invoice, sends it via Gmail to the client, and updates the invoice status once the email is sent.
All steps are fully automated with minimal manual effort.

🔁 Workflow Architecture
1. Manual Trigger

Workflow starts when “Execute workflow” is clicked.

Can be replaced with Cron trigger for scheduled billing cycles.

2. Fetch Invoice Data from Google Sheets

Reads rows containing:

Client name

Email address

Invoice number

Amount

Due date

Status

Each row represents one invoice.

3. Loop Over Invoices

Processes invoices one by one.

Ensures safe execution and accurate status tracking.

4. Template Rendering (Invoice Layout)

Uses a Templated / Render node to create a structured invoice layout.

Dynamically injects:

Client details

Invoice ID

Amount, tax, and total

Due date

5. HTTP Request (Invoice Generation)

Sends invoice data to an external service or internal endpoint.

Generates a PDF invoice based on the template.

Returns a downloadable invoice file.

6. JavaScript Code Node

Formats email content.

Attaches the generated invoice PDF.

Prepares clean subject & body text.

7. Send Invoice via Gmail

Sends a professional invoice email with:

Subject line

Personalized message

PDF invoice attachment

📧 Example:

Invoice INV-0158 – Payment Due on 28-11-2025

8. Update Invoice Status in Google Sheets

Updates the row with:

Status: SENT / UNREAD

Timestamp

Maintains a clear billing audit trail.

📧 Sample Email Output

Personalized greeting

Invoice reference number

Amount & due date mentioned clearly

PDF invoice attached

This ensures professional and reliable communication with clients.

📄 Sample Invoice Details

Client Name & Address

Invoice Number

Invoice Date & Due Date

Line Items (Services)

Tax calculation

Total payable amount

🛠️ Tech Stack

n8n – Workflow automation

Google Sheets API – Invoice data storage

Gmail API – Email delivery

HTTP API – Invoice PDF generation

JavaScript – Data formatting & logic

✨ Key Features

✅ Automated invoice generation

✅ Dynamic PDF invoices

✅ Email delivery with attachments

✅ Google Sheets status tracking

✅ Scalable billing workflow

✅ Minimal manual intervention

🔮 Future Enhancements

Add Cron scheduling (monthly billing)

Integrate payment links (Stripe/Razorpay)

Add payment confirmation tracking

Auto-send reminders for overdue invoices

Store invoices in Google Drive

🎯 Use Cases

Freelancers sending monthly invoices

Startup client billing

Agency retainers

Subscription-based services

Automated finance workflows

👩‍💻 Author

Triman Kaur
Web Developer | Automation & AI Enthusiast



Is this conversation helpful so far?

ChatGPT can make mistakes. C
