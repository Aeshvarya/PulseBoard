# 📡 PulseBoard

> **The Jarvis of your campus schedule.** Reads college emails, finds events with AI, and makes sure students never miss what's happening on campus.

Every semester students miss events — not from laziness, but because info is scattered across emails, WhatsApp groups, and "that one friend who forgets to tell." PulseBoard becomes the **single source of truth**: it ingests college emails, auto-extracts event details, and delivers a personalized, real-time event feed to every student's phone.

Built for **Winter of Code '26 (WOC)** by a team of 6.

---

## ✨ What it does

**📧 Email Intelligence Engine**
- Parses college emails (HTML, PDF, images) via IMAP
- Auto-detects event details — time, venue, organizer, reschedules — using **Gemini AI**
- Smart filtering to drop spam; special handling for OAs, interviews, and personalized notices

**📅 Real-Time Event Radar**
- Live dashboard of what's happening on campus right now
- Calendar/timeline view with club & topic filters
- Customizable notification reminders

**🎪 Club Portal**
- Clubs push events live (title, media, tags)
- Clash detection — warns clubs of scheduling conflicts
- Engagement polls + event media uploads

**🎯 Student Personalization**
- Follow clubs/topics → personalized feed
- Recommender for similar events
- Private interview/OA notices visible only to relevant students

## 🛠 Tech Stack

**Backend** (Node + TypeScript)
- Express, MongoDB / Mongoose
- **Auth & security:** JWT, bcrypt, **2FA (TOTP via speakeasy + QR)**, Google OAuth, helmet/cors
- **AI:** Google Gemini — email → structured event extraction
- **Email pipeline:** IMAP (imapflow), mailparser, Nodemailer + SendGrid
- **Infra:** Cloudinary (media), node-cron (scheduled polling), chrono-node (NL date parsing)
- Clean MVC: controllers / services / models / routes / jobs / middlewares

**Mobile** (Expo / React Native + TypeScript)
- expo-router, push notifications, auth sessions, image picker
- NativeWind (Tailwind), Reanimated + Moti animations

## 👤 My role — Backend Lead

I owned the backend: the **Express + MongoDB API**, the **email intelligence pipeline** (IMAP ingestion → Gemini AI event extraction → notifications), **auth & security** (JWT, 2FA, Google OAuth), and the **cron-based real-time engine**. Worked in a team of 6, with the server-side architecture and AI/email core being my responsibility.

## 📄 Docs
Full technical documentation in [`/docs`](./docs).

---

*Team of 6 · Winter of Code 2026 · IIT Jodhpur*
