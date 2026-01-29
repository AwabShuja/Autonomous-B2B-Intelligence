# 🚀 Autonomous B2B Intelligence: AI-Powered Research & Outreach Engine

## **Overview**
This repository contains a high-performance **Autonomous Sales Intelligence Pipeline** engineered in **n8n**. It solves the problem of manual B2B lead research by leveraging **Agentic AI** to crawl live company websites, perform deep strategic analysis, and generate hyper-personalized outreach content at scale.



---

## **💼 Business Value Proposition**
* **Eliminate Manual Research:** Automates the "Deep Research" phase that typically takes sales reps 20-30 minutes per lead.
* **Identify Real Business Gaps:** Uses LLMs to identify actual operational pain points on a prospect's website rather than sending generic templates.
* **Human-in-the-Loop:** Combines the speed of AI with human oversight via real-time Discord notifications.
* **Data Enrichment:** Automatically transforms a simple "Company Name" and "URL" into a full-scale sales strategy in your database.

---

## **🛠️ Technical Architecture**
The system is built as a modular pipeline with the following logic:

### **1. Trigger & Intake**
* **Source:** Google Sheets API.
* **Logic:** Real-time polling for new rows added to the `AI_Growth_Leads` spreadsheet.

### **2. Live Web Scraping**
* **Tool:** **Firecrawl API**.
* **Process:** Navigates to the prospect's URL and extracts content as clean **Markdown**. This ensures the AI receives structured text instead of messy HTML, reducing token usage and improving accuracy.

### **3. Strategic Intelligence (The AI Brain)**
* **Model:** **Google Gemini 1.5 Flash**.
* **Role:** Acts as a Senior B2B Strategy Consultant.
* **Output Parsing:** Uses a **Structured Output Parser (JSON)** to ensure the AI's response is divided into two distinct fields:
    * `research_summary`: A 2-sentence breakdown of the company's biggest "Gap."
    * `personalized_pitch`: A high-conversion outreach email focused on an AI solution.

### **4. Database Synchronization**
* **Update Logic:** Uses the **Website URL** as a unique key to locate the original row and update the `Research Summary`, `Personalized Pitch`, and `Status` columns.

### **5. Real-Time Alerts**
* **Integration:** Discord Webhooks.
* **Function:** Sends a formatted alert with the company name and pitch preview, allowing for immediate manual follow-up.

---

## **🚀 Implementation Details**
* **Orchestration:** n8n (Low-Code Workflow Automation)
* **LLM Framework:** LangChain (via n8n nodes)
* **Data Persistence:** Google Workspace Integration
* **API Standards:** REST, Webhooks, JSON Schema

## **📦 How to Deploy**
1. **Clone/Download**: Save the `B2B_AI_Strategy_Consultant.json` file from this repository.
2. **Import**: Open n8n and select **Import from File**.
3. **Configure Credentials**:
    * **Google Sheets**: Set up OAuth2 credentials.
    * **Firecrawl**: Insert your API key.
    * **Gemini**: Insert your API key from Google AI Studio.
    * **Discord**: Add your server's Webhook URL.
4. **Sheet Setup**: Create a sheet with these headers: `Company Name`, `Website URL`, `Research Summary`, `Personalized Pitch`, `Status`.

---

## **🎯 Technical Skills Demonstrated**
* **Agentic AI Workflow Design**
* **Structured Data Extraction (JSON)**
* **API Integration & Webhooks**
* **Data Engineering & Persistence**
* **LLM Persona Engineering**

