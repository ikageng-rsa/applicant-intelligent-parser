# 🧠 Applicant Intelligent Parser (Make.com Workflow)

![Screenshot](make.com%20screenshot.png)


This automation processes job applications submitted via Google Forms. It uses AI to extract and evaluate candidate information, score applicants based on suitability, and optionally routes top candidates through a human approval flow.

Built with [Make.com](https://make.com), this workflow simulates a real-world HR automation pipeline using AI, conditional logic, and structured Google integrations.

---

## ⚙️ Workflow Overview

### 🟢 Google Forms Intake
- Listens for new Google Form submissions
- Captures form responses including CV file links and basic applicant info

### 🧠 AI-Powered Parsing & Evaluation
- Fetches the applicant's CV (if linked) from Drive
- Uses LLM (OpenAI or Gemini) to extract:
  - Full Name
  - Email
  - Phone
  - Skills
  - Qualifications
  - Experience
- AI model also scores the applicant for role-fit based on predefined criteria

### 📊 Shortlist Logging
- Logs structured results and AI score to Google Sheets

### 🧑‍⚖️ Human-in-the-Loop
- Filters applicants with high scores (e.g.7)
- Sends approval request via email or Telegram
- Waits for response (Approve/Reject) via webhook
- Logs approval decision in Sheets

---

## 🧰 Stack

- **Make.com** workflow builder
- **Google Forms + Sheets + Drive**
- **OpenAI / Gemini AI API**
- **Webhooks** for HITL response handling

---

## 🗂 Included File

- `Applicant Intelligent Parser.blueprint.json` – Make.com main scenario file
- `Applicant Intelligent Parser Telegram Request Webhook.blueprint.json` – Make.com webhook scenario file

> ⚡ To use: Import into Make.com, connect your services, and customize your scoring prompts or filters as needed.

---

## ✅ Use Case

> Automate the evaluation and shortlisting of applicants for any hiring process, reducing bias, increasing speed, and enabling structured decision-making.

---

## Setup Instructions for Make.com Blueprint:

1. Go to **all the Google modules** (Google Drive, Google Sheets & Google Forms) and add a **connection**.
2. Go to the **Google Gemini modules** (CV Parser & Applicant Scorer) and add your **API key**.
3. Go to the **Telegram module** and add:
   - Your **Bot Token**
   - Your **Chat ID** (You can get it by sending a message to [@RawDataBot](https://t.me/RawDataBot) on Telegram)

---

## 📝 Google Form Template

This blueprint uses a Google Form. Click below to make a copy:

👉 [Use the Google Form Template](https://docs.google.com/forms/d/1MaAbL8rk_ejrm2jsOslT_LSYpZilKXu6O02tFn__BKs/copy)

> After copying, you can customize the form and connect it to your Make scenario as needed.
