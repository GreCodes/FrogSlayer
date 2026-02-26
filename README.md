# 🐸 FrogSlayer

FrogSlayer is an event-driven productivity automation built with **n8n** that helps overcome procrastination by sending a daily priority task via Telegram and allowing users to mark it complete with a simple command.

---

## 🎬 Demo

![FrogSlayer demo](https://github.com/GreCodes/FrogSlayer/blob/main/docs/FrogSlayerDemo.gif?raw=true)


---

## 🧠 Overview

FrogSlayer automates the [“eat the frog”](https://www.tempo.io/blog/eat-the-frog) method by reducing decision fatigue and creating a simple feedback loop for task completion.

Each day at 8:00 AM, the system automatically selects the highest-priority unfinished task from a Google Sheet and sends it to Telegram.
When the task is completed, the user replies with /done, and the task status is updated in Google Sheets. An affirming confirmation message is then sent via Telegram.

This project demonstrates workflow automation, API integration, and event-driven architecture.

---

## ⚙️ How It Works

### 1️⃣ Daily Task Notification

- Trigger: Scheduled (every day at 8:00 AM)  
- Fetches tasks from Google Sheets  
- Selects the first incomplete task  
- Sends task details via Telegram


### 2️⃣ Mark Task Completed

- Trigger: Telegram command (`/done`)
- Identifies the active task
- Updates task status in Google Sheets
- Sends confirmation message

---

## 🖼 Workflow Walkthrough

### Daily Task Notification Workflow

Runs automatically every day at 8:00 AM.
It retrieves the highest-priority incomplete task from Google Sheets and sends it to Telegram, ensuring the user starts the day with a clear focus.

### Task Completion Workflow

Triggered when the user sends /done in Telegram.
The workflow validates the command, updates the task status in Google Sheets, and sends an affirming confirmation message, closing the feedback loop.

---

## 🧩 Architecture

Scheduler → Task Selection → Telegram Notification
Telegram Command → Update Task → Confirmation Message

---

## 🛠 Tech Stack

- **n8n** — workflow automation
- **Google Sheets API** — task storage
- **Telegram Bot API** — notifications & interaction
- **JavaScript** — workflow logic

---

## 🎯 Why I Built This

I created FrogSlayer to explore how automation can reduce friction in daily workflows and support consistent task completion.

The project also helped me practice designing modular workflows, handling state across external systems, and building user-friendly automation loops.

---

## 🚀 Key Learnings

- Designing modular, event-driven workflows
- Integrating multiple external APIs
- Managing state across automation steps
- Building conversational automation flows
- Debugging and troubleshooting automation logic

---

## 🔮 Future Improvements

- Streak tracking
- Weekly summaries
- Priority-based task scoring
- Simple dashboard UI

---

## 📌 Project Status

Active personal project used for experimentation with workflow automation and integrations.
