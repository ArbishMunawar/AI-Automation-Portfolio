# Day 5: AI Blog Generator 🤖📝

Welcome to Day 5 of my AI Automation & Development challenge! This project is an automated content generation workflow built using **n8n**. It takes a simple topic input, uses an AI model to draft a complete, structured blog post, and automatically saves the final article as a new document in Google Docs.

## 🚀 Overview

Manually researching and formatting blogs takes time. This workflow completely automates the drafting phase. By submitting a single topic, the system uses an AI orchestrator to write a structured post and pushes it instantly to cloud storage for editing.

### Workflow Architecture
`Manual Trigger` ➔ `Set Topic` ➔ `AI Chat Node` ➔ `Google Docs Node`

---

## 🛠️ Tech Stack & Tools

* **Automation Platform:** [n8n]
* **AI Model:** Google Gemini / OpenAI (Advanced AI Text Generation)
* **Cloud Storage:** Google Docs (via Google Workspace API)

---

## 📋 Features

* **Dynamic Input Handling:** Enter any topic in a centralized `Set` node without breaking the underlying prompt structure.
* **Auto-Formatting:** Generates clean content sections including introductions, headings, sub-points, and conclusions.
* **Seamless Cloud Delivery:** Automatically authenticates and outputs directly into your personal Google Drive as a ready-to-edit document.

---

## 🔧 How It Works (Step-by-Step)

1. **Manual Trigger:** Starts the workflow execution manually during testing phases.
2. **Set Node:** Stores your target blog topic into a field named `topic` (e.g., *Benefits of AI automation for small businesses*).
3. **AI Chat Model:** References the variable expression `{{ $json.topic }}` and passes it to the AI model with specialized styling instructions.
4. **Google Docs Node:** Uses the `Create` operation to open a brand-new document using the topic as the title, and maps the AI response directly into the document body.

---

## 📈 Future Enhancements

* [ ] Replace the manual trigger with a **Google Form** or **Webhook** for automatic submissions.
* [ ] Integrate a **Google Sheets** node to log the generation date and matching document links.
* [ ] Add a **Schedule Trigger** to auto-generate content weekly based on an automated queue.

---
*Created as part of my portfolio building journey in AI Automation.*