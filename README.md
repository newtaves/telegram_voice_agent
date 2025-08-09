📅 Telegram AI Appointment Scheduler – n8n Workflow
This repository contains an n8n workflow that integrates Telegram, Google Gemini AI, Google Calendar, and Google Sheets to create an AI-powered appointment scheduling assistant.

🚀 Features
📩 Accepts messages or voice notes from Telegram users.

🗣 Transcribes audio messages into text.

🤖 Uses Google Gemini AI to understand user intent and process requests.

📅 Creates, retrieves, and deletes events in Google Calendar.

📊 Reads appointment data from Google Sheets.

💾 Stores conversation memory for better AI context.

📤 Sends replies back to Telegram.

📌 Workflow Overview

1. Telegram Trigger
Starts the workflow when a Telegram user sends a message or voice note.

2. Switch (Mode: Rules)
Separates processing for:

Text messages → Directly sent for AI processing.

Voice messages → File is downloaded and transcribed before processing.

3. Get a File & Transcribe a Recording
Downloads voice note from Telegram.

Uses transcription service to convert audio into text.

4. Edit Fields
Formats and cleans message text for AI.

5. AI Agent
Uses Google Gemini Chat Model for natural language understanding.

Accesses Simple Memory for conversation continuity.

Executes different Google Calendar and Google Sheets operations:

Create event

Get events

Delete event

Retrieve sheet data

6. Send a Text Message
Sends AI-generated responses back to the Telegram user.

🛠 Prerequisites
n8n installed locally or on a server.

Telegram Bot Token from BotFather.

Google Cloud Project with:

Google Calendar API enabled

Google Sheets API enabled

Service account credentials

Google Gemini API access.

Transcription API credentials (if using external service).

⚙️ Setup Instructions
Import the Workflow

Open n8n → Workflows → Import from File.

Upload the provided JSON file.

Configure Telegram Trigger

Set your bot token.

Configure updates for messages and voice notes.

Set API Credentials in n8n:

Google Calendar

Google Sheets

Google Gemini Chat Model

(Optional) Audio transcription service

Test the Workflow

Send a text or voice message to your Telegram bot.

The AI will understand your request and update Google Calendar/Sheets accordingly.

📄 Example Usage
User:

"Book a meeting with John tomorrow at 3 PM."

AI Response:
✅ "Your meeting with John has been added to Google Calendar for tomorrow at 3:00 PM."

📜 License
This project is licensed under the MIT License.
