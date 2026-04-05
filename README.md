# AI-Agent-chatbot-telegram-websearch-serp-googlesheet
🚀 AI-Powered Lead Generation Pipeline

An automated, bulletproof Full-Stack Lead Generation backend built using n8n, Groq (Llama 3), SerpAPI, and Google Sheets. This system takes user input via Telegram, autonomously researches the web, formats the data into JSON, and saves it into a database without any human intervention.

🏗️ Architecture

Frontend (Telegram): Acts as the UI where the user sends a company name or phone number.

AI Orchestrator (n8n + Groq/Llama 3): The brain of the operation. It decides which tools to use and processes the natural language into structured JSON.

Research Tool (SerpAPI): Dynamically searches the web for Business Name, Owner, Address, and Contact Info.

Database (Google Sheets): Connected via a Google Cloud Service Account to securely store the extracted leads.

✨ Key Features & Engineering

Linear Data Pipeline: Bypassed standard tool constraints by decoupling the AI Agent and the Database into a linear pipeline, parsing raw JSON using JavaScript expressions {{ JSON.parse($json.text).BusinessName }}.

Bulletproof Error Handling: Implemented IF nodes and logical routing. If the AI cannot find data (e.g., fake companies), the system routes to a fallback Telegram message instead of crashing.

Fallback Values: Engineered JS default values (|| "N/A") to handle missing JSON keys seamlessly.

Strict Schema Enforcement: Overcame schema validation errors by enforcing zero-space column names and strict prompt conditioning.

💻 Local Development Setup (Phase 4)

This project also marks the transition to a local Python development environment for advanced API handling and data processing.

Prerequisites

Python 3.11+

VS Code

Installation

Clone the repository:

git clone [https://github.com/yourusername/ai-lead-gen-pipeline.git](https://github.com/yourusername/ai-lead-gen-pipeline.git)
cd ai-lead-gen-pipeline


Create and activate a virtual environment:

python -m venv ai_env
# On Windows:
ai_env\Scripts\activate
# On Mac/Linux:
source ai_env/bin/activate


Install dependencies:

pip install requests pandas python-dotenv


🧠 Lessons Learned

Handling AI Hallucinations during tool calls.

Managing JSON parsing and schema validation in No-Code/Low-Code platforms.

Setting up secure Google Cloud Service Accounts for automated database entries.

Built with ❤️ during Day 12 of my AI & Automation Journey.
