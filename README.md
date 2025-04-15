# 📄 Project Brief: USSD-Enabled Pest & Disease Reporting System

**Project Name:**  
**AgriAlert** – USSD-Based Pest & Disease Early Warning and Advisory System

**Submitted By:**  
Benjamin Ohene-Adu 
**Date:**  
14th April 2025

---

## 1. ✅ Project Overview

AgriAlert is a full-stack, USSD/SMS-enabled pest and disease reporting and advisory platform for smallholder farmers in rural regions. The system enables farmers to report crop health issues via SMS/USSD in local languages, while agricultural officers and experts can respond through a web-based dashboard with tailored advice or escalation protocols.

---

## 2. 🎯 Core Objectives

- Enable farmers with basic phones to report pest and disease incidents in real-time via USSD/SMS.
- Log, analyse, and visualise these reports centrally for agricultural officers.
- Automate responses using a knowledge base and send advisories via SMS.
- Provide administrators with tools to track outbreaks geographically and temporally.

---

## 3. 🧰 Tech Stack and System Architecture

| Layer               | Technology Used                 | Notes                               |
|---------------------|---------------------------------|-------------------------------------|
| Frontend UI         | **React.js**                    | Dashboard for admin/ag officers     |
| Backend API         | **Node.js + Express**           | RESTful API, logic, SMS handling    |
| Database            | **MySQL**                       | Farmers, reports, alerts, logs      |
| SMS/USSD Gateway    | **Africa’s Talking** (or Twilio) | Inbound & outbound SMS/USSD        |
| Hosting             | Render / Railway / Vercel       | Modular deployment & scaling        |
| Auth (Optional)     | JWT-based login for officers    | Role-based access control           |
| Language Support    | Multi-language support           | Future-ready for localization      |

---

## 4. 📦 Database Design Overview

### Tables:
- **farmers** – Farmer records, contact, location, language
- **pest_reports** – Reports from farmers (crop, issue, location, time, status)
- **alerts** – SMS messages sent, timestamp, content
- **users** – Admin/AG officer login and permissions (optional)

---

## 5. 📲 USSD/SMS Workflow

1. **Farmer** dials USSD code or sends SMS with crop issue.
2. **SMS Gateway** hits the Node.js webhook endpoint.
3. **Backend API** parses and stores the report.
4. Automated SMS sent acknowledging the report and providing relevant guidance.
5. **Admin Dashboard** updates in real-time for officers to review and act on.

---

## 6. 🧑‍🌾 User Roles

- **Farmers** (via USSD/SMS): Submit crop-related issues and receive tips.
- **Agricultural Officers** (via Web): Monitor and respond to farmer issues.
- **System Admins**: Manage officers, view metrics, edit knowledge base.

---

## 7. 🔒 Security & Best Practices

- Input sanitisation & SQL injection protection
- HTTPS-secured endpoints
- .env-based credential management
- Logging & monitoring for SMS delivery and system usage
- Graceful fallback for SMS failures
- Optional offline-first design via SMS retry queue

---

## 8. 📊 Future Enhancements

- GPS tagging (if smart-featured phones are used)
- AI/ML classification of symptoms (with image support via WhatsApp)
- Integration with government pest outbreak alert systems
- Knowledge base for automated responses
- Offline-first progressive web app (PWA) for field officers

---

## 9. 🧠 Insights & Rationale

- **Accessibility First**: Targeting basic phone users ensures inclusion for remote communities.
- **Timeliness**: Early detection and response help contain pest spread and minimise yield loss.
- **Scalability**: The modular design allows future support for additional services (e.g., weather alerts, market prices).
- **Data Value**: Centralised data offers insights into regional trends and can inform policy or intervention programs.

---

## 10. 📆 Timeline (Suggested)

| Phase                     | Duration        |
|--------------------------|-----------------|
| Requirements & Planning  | 1 week          |
| Backend + DB Setup       | 1 week          |
| Frontend Dashboard       | 1 week          |
| SMS Integration & Testing| 1 week          |
| Pilot Launch             | 1 week          |

---

![image](https://github.com/user-attachments/assets/a702f559-8eaa-45b7-b97d-7d2ccc025c78)

## What It Represents:
- The entry point is a farmer interacting via USSD/SMS.
- A gateway provider (e.g., Africa's Talking or Twilio) forwards the data to your Node.js API.
- The API parses and stores the report in MySQL.
- An acknowledgement SMS is sent automatically.
- The React dashboard reflects updates in real-time.
Officers can respond through the UI, and personalised advisories are sent via SMS.
---
## ✅ Approval Request

This project aligns with our mission to empower farmers with practical tools using accessible technology. We seek your approval to begin development with a phased rollout. All code will follow best practices, and documentation will be provided.


