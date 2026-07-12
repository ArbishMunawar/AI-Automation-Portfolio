# Day 6: AI-Powered Social Media Content Generator 🚀

Welcome to Day 6! Today's project focuses on building an automated **Social Media Content Generator** workflow using **n8n**. This workflow leverages an advanced AI Agent to automatically brainstorm, generate, format, and log digital content seamlessly across different cloud platforms.

## 📋 Workflow Overview

The entire automation pipeline is structured as follows:

1. **Trigger (`On clicking 'Execute workflow'`)**: Initiates the automation manually or via scheduled testing.
2. **Edit Fields**: Sets up the initial configurations, custom raw variables, or niche-specific keywords required for the generation process.
3. **AI Agent + OpenAI Chat Model**: The core engine. Takes the input parameters and uses OpenAI's language model to intelligently draft tailored social media content.
4. **Code in JavaScript**: Cleans, parses, or formats the raw AI output string into structured JSON objects for downstream APIs.
5. **Create a Document (Google Docs)**: Automatically generates a formal backup or detailed copy of the text directly inside Google Drive.
6. **Create a Database Page (Notion)**: Logs the generated content, metadata, and status directly into a centralized Notion content calendar tracking database.

---

## 🛠️ Tech Stack & Integrations

* **Automation Engine:** n8n (Node-based workflow automation)
* **Artificial Intelligence:** OpenAI Chat Model API Integration
* **Cloud Storage:** Google Workspace (Google Docs/Drive API)
* **Productivity & Workspace:** Notion API (Database management)
* **Data Transformation:** Custom JavaScript (ES6+)

---

## 🚀 Setup & Execution Instructions

### 1. Prerequisites
Ensure you have active API credentials and connections configured within your n8n environment for:
* OpenAI
* Google Docs / Google Drive
* Notion

### 2. How to Import the Workflow
1. Create a new workflow in your n8n dashboard.
2. Open the workflow settings and click **Import from File** (or simply copy the JSON representation of this workflow and paste it directly onto the n8n canvas).
3. Connect your active credentials to the **OpenAI Chat Model**, **Create a document**, and **Create a database page** nodes.

### 3. Running the Pipeline
* Click the **Execute workflow** button.
* Watch the data flow seamlessly from raw input, through the AI agent, down to automated documentation and database updates!