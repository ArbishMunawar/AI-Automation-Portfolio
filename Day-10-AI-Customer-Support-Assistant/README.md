# Day 10: AI Customer Support Assistant

An AI-powered customer support automation workflow built using **n8n** and **Google Gemini**. The workflow simulates receiving a customer inquiry, generates a professional response using AI, and automatically sends the reply through Gmail.

## 🚀 Project Overview

This workflow demonstrates how AI can automate customer support by generating accurate, polite, and context-aware email responses. It reduces manual effort while maintaining professional communication.

## 🛠️ Workflow Architecture

```
Manual Trigger
      ↓
Edit Fields (Customer Details)
      ↓
AI Agent (Google Gemini)
      ↓
Gmail (Send Message)
```

## 📌 How It Works

### 1. Manual Trigger
Starts the workflow manually for testing purposes.

### 2. Edit Fields
Provides sample customer information, including:
- Customer Name
- Customer Email
- Email Subject
- Customer Message

### 3. AI Agent (Google Gemini)
The AI reads the customer's inquiry and generates a professional, friendly, and helpful email response.

### 4. Gmail
Automatically sends the AI-generated response to the customer's email address.

## ✨ Features

- AI-generated customer support replies
- Personalized responses using customer name
- Professional email formatting
- Automated email delivery via Gmail
- Beginner-friendly n8n workflow

## 🧰 Technologies Used

- n8n
- Google Gemini AI
- Gmail API

## 📂 Example Input

**Customer Name**
```
John Smith
```

**Subject**
```
Refund Request
```

**Customer Message**
```
Hello,

I accidentally ordered the wrong product. Can I request a refund?

Thank you.
```

## 📤 Example AI Response

```
Hello John Smith,

Thank you for reaching out.

We're sorry to hear that you ordered the wrong product. We'd be happy to assist you with your refund request.

Please reply with your order number so our support team can verify your purchase and begin the refund process.

If you have any further questions, we're here to help.

Best regards,
Customer Support Team
```

## 📚 Learning Outcomes

- Building AI-powered automation with n8n
- Using Google Gemini for email generation
- Passing dynamic data between workflow nodes
- Automating Gmail responses
- Designing practical customer support workflows


