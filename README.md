🤖 Telegram AI Automation using n8n

This project is an AI-powered Telegram bot automation built using n8n.
It listens to incoming Telegram messages, processes them using an AI agent (Google Gemini), and replies automatically.

🚀 Features
📩 Receive messages from Telegram
🧠 Process messages using AI (Google Gemini)
💬 Send intelligent replies automatically
🧠 Optional memory support for context-aware conversations
⚡ Fully automated workflow using n8n
🏗️ Workflow Architecture
Telegram Trigger → AI Agent → Send Message (Telegram)
Components:
Telegram Trigger
Listens for incoming user messages
AI Agent
Uses Google Gemini Chat Model
Optional memory for conversation context
Send Message Node
Sends AI-generated response back to user
🛠️ Prerequisites

Before setup, ensure you have:

Node.js (v18+ recommended)
n8n installed (local or cloud)
Telegram account
Google Gemini API key
⚙️ Installation & Setup
1. Install n8n Locally
npm install n8n -g
n8n start

Open:

http://localhost:5678
2. Create Telegram Bot
Open Telegram and search: @BotFather
Run:
/start
/newbot
Copy your Bot Token
3. Fix Telegram Webhook (IMPORTANT)

Since you're running on localhost, Telegram requires HTTPS.

Option A: Use ngrok (Recommended)
ngrok http 5678

Copy HTTPS URL like:

https://abcd1234.ngrok.io
4. Configure Telegram Node in n8n
Paste Bot Token
Set Webhook URL:
https://your-ngrok-url/webhook
5. Setup Google Gemini API
Go to: https://ai.google.dev
Generate API key
Add in n8n credentials:
Service: Google Gemini
Paste API key
6. Configure AI Agent Node
Connect:
Chat Model → Google Gemini
Memory → Simple Memory (optional)
7. Connect Nodes Properly

Ensure flow:

Telegram Trigger → AI Agent → Send Message
▶️ How to Use
Start n8n
Start ngrok
Activate workflow in n8n
Open your Telegram bot
Send a message

✅ You will receive an AI-generated reply instantly

📂 Example Use Cases
AI Chatbot
Customer Support Automation
Personal Assistant Bot
FAQ Automation
Learning Assistant
