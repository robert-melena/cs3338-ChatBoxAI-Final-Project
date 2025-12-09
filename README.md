# CS 3338 Final Project – ChatBox AI

Team: 
- Robert Melena
- Robert Guiterrez
- Miguel Aguirre

**Jira Project URL:**  
- [https://](https://cs3338-group-01.atlassian.net/jira/software/projects/CAG/boards/67)

---

## Overview

ChatBox AI is a documentation-based final project for CS 3338 that describes the design of a web-based AI chat assistant for university students.

The goal of ChatBox AI is to show how a modern AI chatbot could be structured using a web frontend, backend API, database, Dockerized deployment, and integrations with tools like Jira and TestRail.  
This project focuses on **software engineering artifacts** (SDD, SRS, design spec, workflow, test plans) rather than a fully implemented system.

---

## System Architecture 

ChatBox AI follows a typical three-tier architecture:

1. Frontend (Web UI)**  
   - Provides a chat interface, login/registration, settings, and an admin dashboard.
   - Connects to the backend via REST APIs.

2. Backend (Application Server)**  
   - Handles authentication, chat session management, and communication with the AI provider.
   - Exposes APIs for students and admin users.
   - Includes an “AI adapter” layer to talk to an external LLM API.

3. Database (Data Layer)**  
   - Stores users, chat sessions, and messages.
   - Can be run as a PostgreSQL container in Docker.

An additional external AI Provider (e.g., OpenAI / Anthropic) is assumed, abstracted behind the AI adapter.

---

## Features 

- Student user can:
  - Register and log in.
  - Start new chat sessions with ChatBox AI.
  - View past chat sessions.
  - (Snapshot 2) Export a conversation history.

- Admin user can:
  - View basic usage statistics (total users, sessions, messages).
  - Monitor overall system health (conceptually, via metrics).

- Documentation includes:
  - Software Design Document (SDD).
  - Software Requirements Specification (SRS).
  - User Manual / README (LaTeX).
  - Design Specification.
  - Snapshot Objective document (Snapshots 1–4).
  - TestRail run summaries for Snapshots 2, 3, and 4.
  - Workflow diagram.

---

## Technologies 

This project is **design-only**, but assumes the following stack in a real implementation:

- **Frontend:** React or Vue.js, HTML, CSS, JavaScript  
- **Backend:** Node.js / Express 
- **Database:** PostgreSQL  
- **Containerization:** Docker + `docker-compose`  
- **Project Management:** Jira (sprint planning, tasks)  
- **Testing Management:** TestRail (test cases + reports)  
- **Documentation:** LaTeX (`.tex` files in `docs/`)

---

## Repository Layout

- `docs/sdd.tex` – Software Design Document  
- `docs/srs.tex` – Software Requirements Specification  
- `docs/readme.tex` – User manual / detailed README (LaTeX)  
- `docs/design_spec.tex` – Design specification of pages/components  
- `docs/snapshot_objectives.tex` – Snapshot 1–4 objectives & reflections  
- `docs/testrail_snapshot2.tex` – TestRail summary for Snapshot 2  
- `docs/testrail_snapshot3.tex` – TestRail summary for Snapshot 3  
- `docs/testrail_snapshot4.tex` – TestRail summary for Snapshot 4  
- `docs/workflow_diagram.tex` – LaTeX wrapper for the overall workflow diagram  
- `docs/images/workflow.png` – High-level architecture diagram  
- `docker-compose.yml` – Conceptual Docker setup for frontend, backend, DB  
- `final-project.txt` – Short project description text file  
- `README.md` – This file (GitHub landing page)

---

## How to View the LaTeX Documents

1. Navigate to the `docs/` folder.  
2. Open a `.tex` file in a LaTeX editor (Overleaf, TeXShop, etc.).  
3. Compile to PDF to view the formatted document.

No actual code is required to run for this course project; the focus is on the design and documentation artifacts.
