# CS 3338 Final Project – ChatBox AI

## Team Members
- Robert Melena  
- Robert Guiterrez  
- Miguel Aguirre  

**Jira Project URL:**  
https://cs3338-group-01.atlassian.net/jira/software/projects/CAG/boards/67

---

## Overview

ChatBox AI is our final project for CS 3338. This project focuses on understanding and documenting the full software engineering process.

The idea behind ChatBox AI is a simple AI chat assistant for students. This project shows how a system like this could be structured using a frontend, backend, database, Docker, Jira, and TestRail.

---

## System Architecture (Conceptual)

### Frontend (Web UI)
- Chat message interface  
- Login / register  
- Settings page  
- Admin dashboard  
- Communicates with backend using REST APIs  

### Backend (Server)
- Handles authentication  
- Stores chat sessions + messages  
- Connects to an AI provider using an **AI Adapter**  

### Database
- Stores users  
- Stores chat history  
- Would run in PostgreSQL via Docker  

---

## Features

### Student Features
- Register and log in  
- Start chat sessions  
- View older sessions  
- Export chat history *(Snapshot 2)*  

### Admin Features
- View total users  
- View total chat sessions and messages  
- Basic system activity overview  

### Documentation Included
- Software Design Document (SDD)  
- Software Requirements Specification (SRS)  
- User Manual (LaTeX)  
- Design Specification  
- Snapshot Objectives (1–4)  
- TestRail PDF reports (Snapshots 2, 3, 4)  
- Workflow diagram  

---

## Technologies

- Frontend: Javascript + CSS  
- Backend: Node.js + Express  
- Database: PostgreSQL  
- Containers: Docker + docker-compose  
- Task Management: Jira  
- Testing: TestRail  
- Documentation: LaTeX  

---

## Repository Layout

```text
docs/
 ├── design_spec.tex
 ├── readme.tex
 ├── sdd.tex
 ├── srs.tex
 ├── snapshot_objectives.tex
 ├── testrail_snapshot2.pdf
 ├── testrail_snapshot3.pdf
 ├── testrail_snapshot4.pdf
 ├── workflow_diagram.tex
 └── images/
      └── workflow.png

docker-compose.yml
final-project.txt
README.md

Go to the docs/ folder
Choose any .tex file
Open it in Overleaf, TeXShop, or another LaTeX editor
Compile to PDF
