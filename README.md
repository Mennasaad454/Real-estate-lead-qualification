# Real Estate Lead Qualification Bot

An AI-powered Telegram bot built with **n8n**, **OpenAI**, and **Google Sheets** to automate real estate lead qualification, scoring, and routing.

---

## Features

- AI-driven lead conversation via Telegram
- Smart field-by-field data collection (no repetition)
- Internal lead scoring (0–100, hidden from user)
- Auto-save leads to Google Sheets
- Conditional routing based on score:
  - **High score (≥80)** → Prompt for appointment
  - **Low score (<80)** → Agent follow-up only

---

## Workflow Overview

1. **Trigger** – Telegram message starts the flow
2. **Conversation** – OpenAI agent collects:
   - Property type
   - Buy or Rent
   - New or Resale
   - First purchase?
   - Timeline
   - Budget
   - Name, Email, Phone
3. **Confirmation** – User verifies collected data
4. **Scoring** – Lead scored internally (based on defined criteria)
5. **Saving** – Lead + score stored in Google Sheets
6. **Routing** – Action taken based on score

---

## Tech Stack

- **n8n** – Automation platform
- **OpenAI GPT-4o** – Lead conversation
- **LangChain Agent** – AI orchestration
- **Telegram Bot API** – User interface
- **Google Sheets** – Lead storage

---

## 🛠 Setup

1. Import the workflow into your n8n instance
2. Configure:
   - OpenAI API credentials
   - Telegram bot credentials
   - Google Sheet (connected with OAuth)
3. Deploy and activate the workflow
