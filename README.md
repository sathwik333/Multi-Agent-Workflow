# 🤖 Multi-Agent Workflow Automation using n8n + LangChain

This project is a fully functional **multi-agent orchestration system** built using [n8n](https://n8n.io) and [LangChain](https://www.langchain.com/). It intelligently routes user requests to specialized agents like email, calendar, contact, or content creation — all through a **single parent AI assistant** powered by LLMs. It supports **voice and text** inputs via Telegram and can be extended to automate any domain task.

---

## ✨ Features

- 🧠 **Ultimate Assistant** — The central brain that decides which agent should handle the user’s request
- 🔀 **Agent Routing** — Modular sub-agents for handling:
  - 📧 Emails
  - 📅 Calendar events
  - 👤 Contacts
  - ✍️ Blog/content creation
- 🎙️ **Telegram Integration** — Accepts both text and voice inputs from users
- 🤔 **Reasoning Engine** — “Think” tool used to validate decisions before execution
- 🧾 **Transcription** — Voice-to-text powered by OpenAI Whisper
- 🔗 **API Integrations** — Supports Google, Airtable, Tavily, and more

---

## 📁 Project Structure

multi-agent-workflow/
│
├── agents/
│ ├── email-agent.json
│ ├── calendar-agent.json
│ ├── contact-agent.json
│ └── content-creator-agent.json
│
├── main/
│ └── ultimate-assistant.json
│
├── README.md
├── LICENSE


---

## ⚙️ Setup Instructions

### 1. Clone the Repo

git clone https://github.com/your-username/multi-agent-workflow.git
cd multi-agent-workflow 
2. Import Workflows into n8n
Import each JSON file in the main/ and agents/ folders into your n8n instance.

Use the “Execute Workflow” Trigger for agent sub-workflows.

3. Configure the Telegram Bot
Create a Telegram Bot using @BotFather

Connect the bot token in n8n’s Telegram Trigger

Replace the Webhook ID if necessary

4. Set Up Credentials
Ensure the following credentials are added in n8n:

🔑 OpenAI or Google Chat model

🧠 Tavily API key (optional for web search)

📧 Google account (for calendar & email)

🗃️ Airtable (for contacts, if used)

💬 Telegram Bot

🚀 Example Use Cases
“Send an email to John asking about the meeting.”

🔎 Contact Agent fetches email

📧 Email Agent sends the message

“Create a calendar event for lunch with Sarah tomorrow.”

🔎 Contact Agent → 📅 Calendar Agent

“Write a blog post about the future of automation.”

✍️ Content Creator Agent

“What’s the capital of Finland?”

🌐 Uses Tavily Search Tool

🛠️ Tech Stack
Tool	Purpose
n8n	Visual workflow automation
LangChain	Agent framework + LLM routing
OpenAI/GPT	Natural language understanding
Telegram API	User input (text + voice)
Tavily	Web search (optional)
Airtable	Contact storage (optional)

🎯 Goals of This Project
Showcase agent-based automation in real-world workflows

Enable voice-driven task execution via LLMs

Modularize agents for maximum reusability and scalability

Build a human-assistant-like experience powered by AI

📜 License
This project is licensed under the MIT License.

