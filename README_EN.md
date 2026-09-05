# 💬 AI-Powered WhatsApp Booking Assistant (n8n + OpenAI + Google Calendar)

This project is an end-to-end automation that allows customers to book, reschedule, and cancel appointments via WhatsApp using natural language. The system understands the message with AI, checks Google Calendar availability, handles conflicts, and creates the appointment.

## 🧠 How It Works
1. **WhatsApp Trigger:** Customer sends a message like "I want a haircut tomorrow at 2 PM".
2. **Message Normalization:** The message is cleaned and the operation type (create, cancel, query, etc.) is determined.
3. **AI Agent:** OpenAI (gpt-4.1-mini) analyzes the message and extracts name, date, time, and service info as JSON.
4. **Date/Time Resolution:** Relative phrases like "tomorrow" or "Friday" are converted to actual dates and ISO formats.
5. **Calendar Conflict Check:** Google Calendar is checked for overlaps. If busy, alternatives are shown.
6. **Appointment Creation:** A calendar event is created when a slot is found.
7. **Database Record:** Appointment details are saved to Google Sheets (customer database).
8. **Response:** The customer is notified via WhatsApp with confirmation.

## 🛠️ Tech Stack
- n8n, WhatsApp Business API, OpenAI GPT-4.1-mini, Google Calendar API, Google Sheets API

## ⚙️ Setup
1. Import `workflow.json` into n8n.
2. Update all Credentials with your own accounts:
   - **WhatsApp Business API**
   - **OpenAI**
   - **Google Calendar**
   - **Google Sheets**
3. Update the calendar and database sheet IDs you want to use.

## 🔒 Security
No real API keys or credentials are included. All fields are replaced with `YOUR_...` placeholders. Customer data and personal information are not included in the file.

## 📷 Preview
![Workflow Schema](images/workflow.png)

## 🎓 Author
This project was designed and developed independently by a self-taught developer focused on n8n and AI automation for personal learning and practice.