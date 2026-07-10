# Day 04: AI Resume Analyzer Workflow 🚀

An automated AI-powered Resume Analyzer built using **n8n**. This workflow accepts an uploaded resume file (PDF or DOCX) via a Webhook, extracts its text content, leverages an AI model to evaluate strengths, gaps, and an overall fit score, and automatically logs the analysis results into a Google Sheet.

## 📋 Workflow Overview

The automation follows a structured 4-step pipeline:

1. **Webhook (Trigger):** Listens for incoming HTTP POST requests containing the resume file.
2. **Extract Text:** Processes the uploaded binary file (PDF/DOCX) and converts it into readable text.
3. **AI Analysis:** Passes the extracted text to an AI model (e.g., Google Gemini / OpenAI) to analyze technical/soft strengths, identify experience or skill gaps, and calculate a candidate score.
4. **Google Sheets:** Appends a new row with the structured analysis data (Candidate Name, Strengths, Gaps, Score, and Timestamp) for easy tracking.

---

## 🛠️ Prerequisites

Before setting up the workflow, ensure you have the following:

- **n8n Instance:** A running instance of n8n (Local, Cloud, or Docker).
- **Google Account:** Access to Google Sheets with a designated spreadsheet created for logging results.
- **AI API Key:** An API key from an AI provider (e.g., Google AI Studio for Gemini or OpenAI).

---

## 🚀 Setup & Installation

### 1. Google Sheets Preparation
1. Create a new Google Sheet.
2. Add the following column headers in the first row:
   * `Timestamp`
   * `Candidate Name`
   * `Strengths`
   * `Gaps`
   * `Score`
   * `Resume Text Summary`

### 2. Importing the Workflow into n8n
1. Copy the workflow JSON configuration from your n8n canvas.
2. In your n8n dashboard, click on **Decks/Workflows** -> **Add Workflow** (or open a blank canvas).
3. Press `Ctrl + V` (or `Cmd + V` on Mac) to paste the nodes directly onto the canvas, or go to the top right menu and select **Import from File**.

### 3. Node Configuration & Credentials

* **Webhook Node:** 
  * Set the HTTP Method to `POST`.
  * Ensure the binary property is configured to receive file uploads (e.g., key name `file`).
* **Extract Text Node:** 
  * Configure it to read from the binary property name defined in your Webhook node.
* **AI Node (Advanced AI Framework):**
  * Link your AI model provider node (e.g., *Google Gemini Chat Model* or *OpenAI Chat Model*).
  * Insert your API Key credentials.
  * Define the prompt to enforce a structured JSON response containing `strengths`, `gaps`, and `score`.
* **Google Sheets Node:**
  * Connect your Google account credentials.
  * Select the **Append** operation.
  * Map the corresponding expressions from the AI node's output into the Sheet columns.

---

## 🧪 Testing the Workflow

1. Switch the workflow execution mode to **Listen for test event** in n8n.
2. Copy the **Test Webhook URL**.
3. Use a tool like **Postman**, **cURL**, or a frontend form to send a `POST` request with a sample resume attached as form-data:
   ```bash
   curl --location 'YOUR_TEST_WEBHOOK_URL' \
   --form 'file=@"/path/to/sample_resume.pdf"'