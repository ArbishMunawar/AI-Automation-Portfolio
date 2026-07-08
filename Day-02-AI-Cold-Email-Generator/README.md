# Day 2: AI Cold Email Generator & Automated Outreach Pipeline

An automated AI-driven email response and cold outreach pipeline built inside n8n. The system automatically detects inbound interest triggers or application alerts via Gmail, passes the context to a Large Language Model (LLM) to craft a highly targeted, personalized cold email response, and automatically dispatches the customized reply back to the recipient via the Gmail API.

## 🚀 Workflow Architecture

The automated pipeline executes the following sequential steps:

1. **Gmail Trigger:** Detects specific incoming messages or leads in real-time.
2. **Get a Message Node:** Extracts the full metadata, subject lines, and text content of the email.
3. **Advanced AI (Basic LLM Chain):** Feeds the extracted details into the prompt blueprint.
4. **Google Gemini Chat Model:** Generates highly personalized, context-aware email copy (Subject + Body) tailored to the sender's industry or application topic.
5. **Send a Message Node:** Automatically formats and sends the final AI-generated cold email out via Gmail.