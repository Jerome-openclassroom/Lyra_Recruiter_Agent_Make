# Lyra_Recruiter_Agent_Make

This repository contains a fully operational Make.com workflow that automates AI-driven replies to recruiter messages, based on a vector-enriched assistant (GPT-4o). The assistant (Lyra) analyzes the incoming recruiter message and crafts a polite and informed answer, referencing the user's GitHub, ecological projects, and AI competence.

---

## 🔧 Project Structure

```
Lyra_Recruiter_Agent_Make/
│
├── code/
│   └── Workflow.json           # Make.com workflow blueprint
│
├── screenshots/
│   ├── Workflow.png            # Overview of the workflow
│   ├── AI_reply_iD.png         # AI response stored in Google Sheets
│   ├── received_message_iD.png # Received message stored in Google Sheets
│   └── PlainText_AI_Reply.png  # Google Docs: full AI reply
```

---

## 🌐 Description

This project mirrors its [n8n equivalent](https://github.com/Jerome-openclassroom/Lyra_Recruiter_Agent_Reply) but has been adapted to Make for broader compatibility and deployment robustness.

Key features:

- **Webhook** triggering (via Postman) for remote input.
- **Google Docs** to simulate an email message received from a recruiter.
- **GPT-4o assistant** enhanced with a **vector store** ("Fichiers_Lyra_candidatures") via File Search.
- **Text Parser node** to remove unwanted references (e.g., `[4:0†source]`).
- **Google Sheets** logging:
  - Incoming recruiter messages
  - AI replies
  - Thread and message IDs
- The `Thread ID` ensures memory continuity within a given recruiter exchange.

---

## ⚠️ Google Authentication Notes

This project also highlights the limitations of Make's integration with Google services:
- OAuth2 with Gmail was found to be complex and unreliable due to Google restrictions.
- As a workaround, **Google Docs** and **Google Sheets** were chosen for storing and retrieving message content.

This workaround ensures:
- Immediate data persistence
- Simpler authentication within Make
- Full visibility for testing and inspection

---

## 📌 Use Case

This demonstrator showcases how a job seeker or researcher can automate professional communications using:
- AI agents
- Workflow automation
- Persistent memory (via vector store + logs)

It is designed to be understandable by recruiters, engineers, and HR professionals alike.

---

## 📄 License

Open for educational and demonstrative purposes. Attribution encouraged.
