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

## 📘 User Stories – AgriAlert: USSD/SMS-Based Pest & Disease Reporting System
---

## 👨🏾‍🌾 Farmers (End Users)

1. **USSD Access**  
   As a farmer, I want to dial a short USSD code, so that I can report pest or disease issues from my basic mobile phone without internet access.
2. **SMS-Based Reporting**  
   As a farmer, I want to send an SMS with a report, so that I can easily report issues in case I can’t use USSD.
3. **Multi-Language Support**  
   As a farmer, I want to interact with the system in my preferred local language, so that I can understand and use the system easily.
4. **Auto-Acknowledgement**  
   As a farmer, I want to receive an SMS confirmation after submitting a report, so that I know my issue has been received.

5. **Receive Advice**  
   As a farmer, I want to receive timely SMS feedback or advice from agricultural officers, so that I can take the correct action.
---

## 🧑🏽‍💼 Agricultural Officers

6. **Real-Time Dashboard**  
   As an agri officer, I want to view incoming reports on a dashboard, so that I can monitor pest/disease cases in real-time.

7. **Classify Reports**  
   As an agri officer, I want to classify each report by type and severity, so that I can prioritise responses appropriately.

8. **Respond to Reports**  
   As an agri officer, I want to send advice via the dashboard interface, so that farmers receive SMS responses quickly.

9. **Flag Escalated Cases**  
   As an agronomist, I want to escalate severe or unknown cases to a senior agronomist, so that experts can handle complex issues.

10. **Report Analytics**  
   As an agri officer, I want to generate a summary of reports by region, type, and response time, so that I can evaluate outreach effectiveness.

---

## 🛠️ Admin / System Administrator

11. **User Management**  
   As an admin, I want to manage user accounts (agri officers, support staff), so that I can control access levels.

12. **Dashboard Configuration**  
   As an admin, I want to configure region, language, and notification settings, so that the system matches local needs.

13. **Audit Logs**  
   As an admin, I want to see logs of all activities in the system, so that I can trace errors or misuse.

14. **Set Notification Rules**  
   As an admin, I want to define SMS templates and alert thresholds, so that communication is consistent and automated.

---

## 👨🏽‍💻 Developers

15. **API Integration**  
   As a developer, I want to build a webhook to receive USSD/SMS reports and process them by the system.

16. **Data Validation**  
   As a developer, I want to validate user input (e.g., format, content), so that incorrect reports don’t enter the system.

17. **SMS Gateway Integration**  
   As a developer, I want to integrate the app with an SMS gateway (e.g., Twilio, Africa's Talking), so that messages can be sent and received reliably.

18. **USSD Session Management**  
   As a developer, I want to manage the USSD session state so that farmers can easily complete multi-step reports.

19. **Database Schema**  
   As a developer, I want to design tables for reports, users, classifications, and messages, so that the system stores all needed data efficiently.

20. **Security**  
   As a developer, I want to implement access control and input sanitisation to ensure the system's security.

---

## 📈 Optional / Future Enhancements

21. **Offline Sync via Agents**  
   As a field agent, I want to log reports for farmers in remote areas and sync later, so that they’re included even without coverage.

22. **Knowledge Base Lookup**  
   As a farmer, I want to search common pest/disease solutions via USSD, so that I get answers immediately without waiting for an officer.

23. **Report Trends Visualization**  
   As an officer, I want to view map-based trends of reported cases, so that I can identify outbreak zones quickly.

---
## ✅ Approval Request

This project aligns with our mission to empower farmers with practical tools using accessible technology. We seek your approval to begin development with a phased rollout. All code will follow best practices, and documentation will be provided.



