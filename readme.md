# Job Application Tracker

This is a full-stack web application for keeping track of a job search in one place: applications, job ads, CV, reminders and networking contacts.

Built as a two-person group project in the *Webbramverk* (web frameworks) course at Nackademin, January–March 2026.

**Tech stack:** React (Vite, React Router, Tailwind CSS, Recharts, drag-and-drop) · Python FastAPI · SQLAlchemy · PostgreSQL · JWT authentication · Vercel

---

## What a user can do

**Account and CV**
- Register and log in with email and password (passwords are hashed, sessions use JWT tokens).
- Build a CV with personal details, summary, work experience, education and skills.
- Export all personal data as a JSON file, or permanently delete the account (GDPR).

**Dashboard – track applications**
- Add applications with company, role, status, applied date, source and notes.
- Move applications between statuses on a drag-and-drop Kanban board.
- Open an application to see its details, or delete it.

**Job search via Platsbanken**
- Search live Swedish job ads from Arbetsförmedlingen's JobTech API.
- Read the full ad, including required and nice-to-have skills and a link to apply.
- Compare an ad with your own CV and get a match percentage, with matched and missing skills.

---

## My contributions

Here are my main contributions to this project.

**Job applications (backend)**
- Designed the `JobApplication` database model.
- Built the REST API for applications: create, list with status filter, view, update, delete, plus a statistics endpoint.
- Linked applications to users, so each user only sees their own data.

**Dashboard (frontend)**
- Built the main dashboard page: statistic cards, pipeline view, drag-and-drop Kanban board, donut chart, search and filter, and a details popup.
- Built the form for adding applications and the API service layer used to call the backend.
- Added loading states and visual polish, and optimised filtering performance with React's `useMemo`.

**Authentication** (together with my teammate)
- Implemented JWT login with bcrypt password hashing.
- Built the login page, protected routes and token handling in the frontend.
- Wrote a script for creating a test user.
