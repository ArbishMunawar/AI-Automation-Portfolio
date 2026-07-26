# Day 9: AI Meeting Summarizer

An AI-powered meeting summarization workflow built in **n8n**. This automation takes a meeting transcript, analyzes it using Google Gemini, generates a structured meeting summary with key decisions and action items, and automatically saves the summary as a Google Docs document.

## 🚀 Workflow Architecture

The workflow executes the following steps:

1. **Manual Trigger / Input**
   - Starts the workflow.
   - Accepts a meeting transcript.

2. **Edit Fields**
   - Stores and formats the meeting transcript.
   - Passes clean text to the AI model.

3. **AI Agent**
   - Uses **Google Gemini** to analyze the transcript.
   - Generates:
     - Executive Summary
     - Key Decisions
     - Action Items
     - Risks & Blockers
     - Next Meeting Agenda

4. **Google Docs**
   - Creates a new Google Document.
   - Saves the AI-generated meeting summary automatically.

---

## 🛠 Technologies Used

- n8n
- Google Gemini AI
- Google Docs API

---

## 📌 Features

- Automatically summarizes long meeting transcripts.
- Extracts important decisions.
- Identifies action items and owners.
- Highlights risks and blockers.
- Suggests agenda items for the next meeting.
- Saves summaries directly to Google Docs.

---

## 📂 Example Workflow

Meeting Transcript
        ↓
   Edit Fields
        ↓
 Google Gemini AI
        ↓
 Structured Summary
        ↓
 Google Docs

---

## 📖 Sample Output

### Executive Summary
The meeting focused on reviewing marketing performance, discussing campaign improvements, and planning next week's goals.

### Key Decisions
- Increase LinkedIn posting frequency.
- Test new email subject lines.
- Produce short promotional videos.
- Automate lead notification workflow.

### Action Items
- Michael: Create email subject lines.
- Emma: Prepare content calendar.
- Michael: Build lead notification automation.

### Risks
- Low email open rate.
- Slow lead follow-up process.

### Next Meeting Agenda
- Review automation progress.
- Analyze updated marketing metrics.
- Evaluate email campaign performance.

---

## 🎯 Learning Outcomes

Through this project, I learned how to:

- Build AI-powered automation using n8n.
- Integrate Google Gemini into workflows.
- Process and summarize long-form text.
- Generate structured AI responses.
- Create Google Docs automatically from AI output.

