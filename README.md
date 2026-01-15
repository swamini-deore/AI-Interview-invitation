# n8n-automation-project

# 🤖 AI Interview Invitation Automation (n8n)

An **end-to-end interview scheduling and email automation system** built using **n8n**, **Google APIs**, and **OpenAI**.
This workflow automatically schedules interviews and sends AI-generated invitation emails when a candidate is added to Google Sheets.

<img width="1428" height="401" alt="Screenshot 2025-12-23 225846" src="https://github.com/user-attachments/assets/77231e7d-c52d-43c8-9bb2-ffaa506d985d" />


watch link: https://drive.google.com/file/d/1EVZQmztNrpNz6CwXVsP4uMJ81chG7Nkm/view?usp=sharing

---

## 🚀 Project Overview

This automation eliminates manual HR tasks by:

* Monitoring candidate data from Google Sheets
* Automatically selecting the next interview slot
* Creating Google Calendar interview events
* Generating professional interview emails using AI
* Sending branded HTML emails via Gmail

---

## 🧠 How the Workflow Works

1. **Google Sheets Trigger**
te row is added
   * Polls the sheet every minute

2. **Interview Slot Logic (JavaScript)**

   * Fixed interview days: **Monday, Wednesday, Friday**
   * Fixed time: **3:00 PM**
   * Ensures only future slots are selected
   * Automatically calculates end time (1 hour)

3. **Google Calendar Event**

 * Creates an interview event
   * Generates a calendar meeting link

4. **OpenAI (LLM Chain)**

   * Uses GPT model to generate a personalized interview email
   * Includes candidate name, education & calendar link

5. **HTML Email Generator**

   * Builds a modern, responsive interview invitation email
   * Includes CTA button, role badge, and branding

6. **Gmail Integration**

   * Sends the interview email automatically to the candidate

---

## 🛠 Tech Stack

* **n8n** – Workflow automation
* **JavaScript** – Slot calculation & logic
* **Google Sheets API** – Candidate data
* **Google Calendar API** – Interview scheduling
* **Gmail API** – Email sending
* **OpenAI (GPT-4.1-mini)** – AI email writing

---

## 📂 Repository Structure

```
ai-interview-invitation/
│
├── workflow.json     # n8n workflow export
├── README.md         # Project documentation
```

---

## 📌 Use Cases

* HR interview scheduling
* Recruitment automation
* AI-driven candidate communication
* Startup hiring workflows

---

## ✨ Key Highlights

* Fully automated workflow
* No manual email writing
* Professional calendar invites
* Scalable HR solution
* AI-powered communication

---

## 👩‍💻 Author

**Swamini Deore**
Automation & Data Analytics Enthusiast

---

## 🔮 Future Enhancements

* Zoom / Google Meet auto-link
* Interview reminders
* Candidate status tracking
* ATS integration

---

## 📜 License

This project is intended for learning and automation purposes.
