# Day 3: AI-Powered Email Classifier & Sheet Automation Pipeline

An automated backend triage pipeline built inside n8n. The system intercepts inbound corporate emails in real-time, routes the subject lines and snippets through a Large Language Model (LLM) for instant zero-shot classification, and logs structured data directly into an external Google Sheets ledger for analytical overview or secondary workflow routing.

## 🚀 Workflow Architecture

The automated pipeline executes the following sequential steps:

1. **Gmail Trigger:** Listens for incoming messages in real-time.
2. **Get a Message Node:** Fetches full unredacted metadata and structural content from the targeted message ID.
3. **Advanced AI (Basic LLM Chain):** Passes clean metadata fields directly into a strict classification prompt blueprint.
4. **Google Gemini Chat Model:** Processes and tags the email intent based on strict categorical constraints.
5. **Google Sheets Node (Append):** Dynamic variable mapping automatically appends the timestamp, sender email, subject line, and generated category tag as a clean new row.