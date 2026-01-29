🚀 Autonomous B2B Growth Engine: AI-Powered Market Research & Outreach
Executive Summary
This project is a production-ready Autonomous Sales Intelligence Pipeline built in n8n. It eliminates the manual labor of B2B lead research by using Agentic AI to scrape live company websites, perform a SWOT-style gap analysis, and generate hyper-personalized outreach strategies.

💼 Business Use Case
The Problem: Sales teams waste ~70% of their time on manual prospect research and drafting non-generic emails.

The Solution: This workflow automates the entire "Research-to-Pitch" lifecycle, ensuring that every lead is approached with a specific, data-driven value proposition.

The Impact: Reduces lead research time from 30 minutes to under 60 seconds while maintaining a high quality of personalization that mimics a senior consultant.

🛠️ Technical Architecture
The workflow is engineered using a modular, "Human-in-the-loop" architecture:

Data Intake (Google Sheets API): Monitors for new entries in a centralized "Growth Leads" database.

Web Scraping (Firecrawl): Performs real-time extraction of website content, converting complex HTML into clean Markdown for optimized LLM consumption.

Agentic Logic (Google Gemini 1.5 Flash): * Persona: Acts as a world-class B2B Strategy Consultant.

Gap Analysis: Identifies operational inefficiencies on the lead's website where AI/Automation can provide immediate value.

Structured Output: Utilizes a JSON Schema to ensure consistent data extraction for the database.

Data Persistence: Dynamically updates the original Google Sheet with the generated Research Summary, Personalized Pitch, and a "Processed" status.

Human-in-the-Loop Notification (Discord Webhook): Delivers a formatted alert to a Discord channel, allowing a human to review the AI's work and hit "Send" on the pitch.

🚀 Key Features & Implementation Details
Structured Output Parsing: Guaranteed JSON response from LLMs to prevent workflow breaks.

Dynamic Data Mapping: Uses unique identifiers (Website URLs) to match and update data without duplicating entries.

Error Handling: Optimized to handle Discord character limits and API timeouts.

📦 Installation & Setup
Import: Download the B2B_AI_Strategy_Consultant.json file and import it into your n8n canvas.

API Keys: Configure your credentials for:

Google Sheets (OAuth2)

Firecrawl (Web Scraping)

Google Gemini (LLM)

Discord (Webhook URL)

Sheet Setup: Ensure your Google Sheet has the following headers: Company Name, Website URL, Research Summary, Personalized Pitch, Status.

📈 Technical Skills Demonstrated
Workflow Orchestration: n8n

LLM Engineering: Prompt Engineering, System Personas, Structured Output Parsing

API Development: REST, Webhooks, JSON

Full-Stack Automation: Data Persistence and Multi-Tool Integration
