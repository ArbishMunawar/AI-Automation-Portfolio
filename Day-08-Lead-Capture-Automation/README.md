# Day 8: Lead Capture Automation

An automated lead capture workflow built inside **n8n** that collects lead information through a Webhook, stores it in Google Sheets, and instantly sends a confirmation email to the lead using Gmail.

## 🚀 Workflow Architecture

The workflow executes the following steps:

1. **Webhook Trigger**
   - Receives lead data from a website form, Postman, or any external application.
   - Accepts information such as:
     - Name
     - Email
     - Phone
     - Service

2. **Google Sheets (Append Row)**
   - Automatically stores each new lead in a Google Sheet.
   - Creates a simple lead database without any manual work.

3. **Gmail**
   - Sends an automated confirmation or thank-you email to the submitted email address.
   - Can also notify the business owner about the new lead.

## 📥 Example Webhook Request

```json
{
  "name": "John Smith",
  "email": "john@gmail.com",
  "phone": "123456789",
  "service": "Web Development"
}
```


## 🛠️ Technologies Used

- n8n
- Webhook
- Google Sheets
- Gmail API

## 🎯 Learning Outcomes

- Working with Webhooks in n8n
- Receiving JSON data from external applications
- Mapping webhook fields into Google Sheets
- Automating lead management
- Sending dynamic emails with Gmail
- Building a simple CRM-style automation workflow

---

### 🔄 Workflow

Webhook → Google Sheets → Gmail