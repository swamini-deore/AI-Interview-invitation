# AI-Interview-invitation
This project is an AI-powered interview invitation automation system built using n8n, OpenAI, Google Sheets, Google Calendar, and Gmail. It automates the entire process of scheduling interviews and sending personalized email invitations to shortlisted candidates.

When a recruiter or HR manager updates a candidate’s status in Google Sheets, the workflow is automatically triggered. The system then creates a calendar event for the interview, generates a professional and personalized invitation message using AI, and sends it to the candidate via Gmail—without any manual intervention.

This solution eliminates repetitive tasks, reduces human errors, saves time, and ensures consistent communication with candidates. It is especially useful for HR teams, recruiters, and companies that handle a high volume of interview scheduling.


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
