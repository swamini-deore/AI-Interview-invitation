Invitation is sent via Gmail
n8n-automation-project
🤖 AI Interview Invitation Automation (n8n)
An end-to-end interview scheduling and email automation system built using n8n, Google APIs, and OpenAI. This workflow automatically schedules interviews and sends AI-generated invitation emails when a candidate is added to Google Sheets.



<img width="1428" height="401" alt="Screenshot 2025-12-23 225846" src="https://github.com/user-attachments/assets/77231e7d-c52d-43c8-9bb2-ffaa506d985d" />


watch link: https://drive.google.com/file/d/1EVZQmztNrpNz6CwXVsP4uMJ81chG7Nkm/view?usp=sharing

This automation consists of multiple connected components that work together to fully automate the interview invitation process.

1️⃣ Google Sheets Trigger

This component continuously monitors a connected Google Sheet.
Whenever a new row is added or an existing row is updated (for example, when a candidate is marked as Shortlisted), the workflow automatically starts.

Purpose:

Detects candidate updates

Acts as the starting point of the automation

2️⃣ JavaScript Code Node (Pre-processing)

This node is used to clean, validate, and format the data coming from Google Sheets.

Purpose:

Extract candidate name, email, role, and interview date

Check conditions (e.g., only proceed if status = "Shortlisted")

Prepare structured data for the next steps

3️⃣ Google Calendar – Create Event

This component automatically schedules the interview by creating a Google Calendar event.

Purpose:

Sets interview date and time

Adds event title (e.g., Interview with John)

Optionally generates a Google Meet link

Stores interview details

4️⃣ Basic LLM Chain (AI Logic)

This is the brain of the system where AI logic is applied.

Purpose:

Passes candidate and interview details to the AI

Defines prompt structure

Controls how the AI generates responses

5️⃣ OpenAI Chat Model

This component generates a professional and personalized interview invitation message.

Purpose:

Writes human-like emails

Adds polite and professional tone

Personalizes content using candidate details

6️⃣ JavaScript Code Node (Post-processing)

This node formats the AI-generated content into a proper email structure.

Purpose:

Adds subject line

Adds company signature

Adjusts formatting

Prepares final email body

7️⃣ Gmail – Send Message

This is the final step where the interview invitation email is sent.

Purpose:

Sends AI-generated email to the candidate

Uses Gmail API

Ensures fast and automatic communication

🔁 Overall Workflow Summary

HR updates candidate status in Google Sheets

Trigger activates the workflow

Candidate data is processed

Interview event is created in Google Calendar

AI generates a personalized email

Email is formatted

Invitation is sent via Gmail
n8n-automation-project
🤖 AI Interview Invitation Automation (n8n)
An end-to-end interview scheduling and email automation system built using n8n, Google APIs, and OpenAI. This workflow automatically schedules interviews and sends AI-generated invitation emails when a candidate is added to Google Sheets.

Screenshot 2025-12-18 111439
🚀 Project Overview
This automation eliminates manual HR tasks by:

Monitoring candidate data from Google Sheets
Automatically selecting the next interview slot
Creating Google Calendar interview events
Generating professional interview emails using AI
Sending branded HTML emails via Gmail
🧠 How the Workflow Works
Google Sheets Trigger

Triggers when a new candidate row is added
Polls the sheet every minute
Interview Slot Logic (JavaScript)

Fixed interview days: Monday, Wednesday, Friday
Fixed time: 3:00 PM
Ensures only future slots are selected
Automatically calculates end time (1 hour)
Google Calendar Event

Creates an interview event
Generates a calendar meeting link
OpenAI (LLM Chain)

Uses GPT model to generate a personalized interview email
Includes candidate name, education & calendar link
HTML Email Generator

Builds a modern, responsive interview invitation email
Includes CTA button, role badge, and branding
Gmail Integration

Sends the interview email automatically to the candidate
🛠 Tech Stack
n8n – Workflow automation
JavaScript – Slot calculation & logic
Google Sheets API – Candidate data
Google Calendar API – Interview scheduling
Gmail API – Email sending
OpenAI (GPT-4.1-mini) – AI email writing
📂 Repository Structure
ai-interview-invitation/
│
├── workflow.json     # n8n workflow export
├── README.md         # Project documentation
📌 Use Cases
HR interview scheduling
Recruitment automation
AI-driven candidate communication
Startup hiring workflows
✨ Key Highlights
Fully automated workflow
No manual email writing
Professional calendar invites
Scalable HR solution
AI-powered communication
👩‍💻 Author
Komal Mahale Automation & Data Analytics Enthusiast

🔮 Future Enhancements
Zoom / Google Meet auto-link
Interview reminders
Candidate status tracking
ATS integration
📜 License
This project is intended for learning and automation purposes.
