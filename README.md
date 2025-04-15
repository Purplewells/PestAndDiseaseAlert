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
   As an officer, I want to view map-based trends of reported cases so that I can quickly identify outbreak zones.

---
Here's a set of basic database tables and a SQL script you can use to create the minimum viable product (MVP) 
```
-- FARMERS table
CREATE TABLE farmers (
    id INT AUTO_INCREMENT PRIMARY KEY,
    phone_number VARCHAR(15) NOT NULL UNIQUE,
    name VARCHAR(100),
    language_code VARCHAR(10),
    location_id INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- OFFICERS table
CREATE TABLE officers (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    phone_number VARCHAR(15),
    region VARCHAR(100),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- USERS table (for login-based access - officers, admins)
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100) UNIQUE,
    password_hash VARCHAR(255),
    role ENUM('admin', 'officer') NOT NULL,
    officer_id INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (officer_id) REFERENCES officers(id)
);

-- LOCATIONS table
CREATE TABLE locations (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    region_code VARCHAR(10)
);

-- LANGUAGES table
CREATE TABLE languages (
    code VARCHAR(10) PRIMARY KEY,
    name VARCHAR(50)
);

-- REPORTS table
CREATE TABLE reports (
    id INT AUTO_INCREMENT PRIMARY KEY,
    farmer_id INT,
    report_text TEXT,
    report_type ENUM('pest', 'disease', 'other') NOT NULL,
    status ENUM('pending', 'responded', 'escalated') DEFAULT 'pending',
    location_id INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (farmer_id) REFERENCES farmers(id),
    FOREIGN KEY (location_id) REFERENCES locations(id)
);

-- RESPONSES table
CREATE TABLE responses (
    id INT AUTO_INCREMENT PRIMARY KEY,
    report_id INT,
    officer_id INT,
    response_text TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (report_id) REFERENCES reports(id),
    FOREIGN KEY (officer_id) REFERENCES officers(id)
);

-- ALERTS (Admin or system generated)
CREATE TABLE alerts (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255),
    body TEXT,
    created_by INT,
    scheduled_at DATETIME,
    status ENUM('draft', 'scheduled', 'sent') DEFAULT 'draft',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (created_by) REFERENCES users(id)
);

-- ALERT_RECIPIENTS (Track who should receive each alert)
CREATE TABLE alert_recipients (
    id INT AUTO_INCREMENT PRIMARY KEY,
    alert_id INT,
    farmer_id INT,
    sent BOOLEAN DEFAULT FALSE,
    sent_at DATETIME,
    FOREIGN KEY (alert_id) REFERENCES alerts(id),
    FOREIGN KEY (farmer_id) REFERENCES farmers(id)
);

-- KNOWLEDGE BASE
CREATE TABLE knowledge_base (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255),
    body TEXT,
    category VARCHAR(100),
    created_by INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (created_by) REFERENCES users(id)
);

-- FEEDBACK (From farmers)
CREATE TABLE feedback (
    id INT AUTO_INCREMENT PRIMARY KEY,
    farmer_id INT,
    type ENUM('report', 'alert', 'content'),
    reference_id INT,
    feedback_text TEXT,
    rating INT CHECK (rating BETWEEN 1 AND 5),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (farmer_id) REFERENCES farmers(id)
);

-- REPORT_CATEGORIES
CREATE TABLE report_categories (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) UNIQUE
);

-- Add foreign key to reports for categories
ALTER TABLE reports
ADD category_id INT,
ADD FOREIGN KEY (category_id) REFERENCES report_categories(id);

-- ESCALATIONS
CREATE TABLE escalations (
    id INT AUTO_INCREMENT PRIMARY KEY,
    report_id INT,
    escalated_to VARCHAR(255),
    reason TEXT,
    status ENUM('open', 'in_progress', 'resolved') DEFAULT 'open',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (report_id) REFERENCES reports(id)
);

-- MESSAGE_LOGS
CREATE TABLE message_logs (
    id INT AUTO_INCREMENT PRIMARY KEY,
    message_type ENUM('sms', 'ussd'),
    recipient_phone VARCHAR(15),
    content TEXT,
    status ENUM('sent', 'failed', 'queued') DEFAULT 'queued',
    response_code VARCHAR(10),
    sent_at DATETIME
);

-- CONTENT_TRANSLATIONS
CREATE TABLE content_translations (
    id INT AUTO_INCREMENT PRIMARY KEY,
    content_type ENUM('alert', 'knowledge', 'system'),
    reference_id INT,
    language_code VARCHAR(10),
    translated_title VARCHAR(255),
    translated_body TEXT,
    FOREIGN KEY (language_code) REFERENCES languages(code)
);

-- GROUPS (e.g., by region, crop type)
CREATE TABLE groups (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    type ENUM('region', 'crop', 'custom')
);

-- GROUP_MEMBERS
CREATE TABLE group_members (
    id INT AUTO_INCREMENT PRIMARY KEY,
    group_id INT,
    farmer_id INT,
    FOREIGN KEY (group_id) REFERENCES groups(id),
    FOREIGN KEY (farmer_id) REFERENCES farmers(id)
);



```

---

```
-- USERS (Admins or Agents)
INSERT INTO users (name, email, password_hash) VALUES
('Admin One', 'admin1@agrohub.test', 'hashed_password_1'),
('Agent Grace', 'grace@agrohub.test', 'hashed_password_2');

-- FARMERS
INSERT INTO farmers (name, phone_number, location) VALUES
('John Doe', '+254700111222', 'Kiambu'),
('Mary Achieng', '+254711222333', 'Kisumu'),
('Ali Musa', '+254722333444', 'Garissa');

-- ALERTS
INSERT INTO alerts (title, body, created_by, scheduled_at, status) VALUES
('Heavy Rain Warning', 'Heavy rain expected in your area. Harvest early.', 1, '2025-04-18 08:00:00', 'scheduled'),
('Maize Pest Alert', 'Early signs of Fall Armyworm infestation reported.', 2, '2025-04-17 10:00:00', 'scheduled');

-- ALERT RECIPIENTS
INSERT INTO alert_recipients (alert_id, farmer_id, sent) VALUES
(1, 1, 0),
(1, 2, 0),
(2, 3, 0);

-- REPORT CATEGORIES
INSERT INTO report_categories (name) VALUES
('Pest Infestation'), ('Disease'), ('Weather Damage'), ('Crop Yield');

-- REPORTS
INSERT INTO reports (farmer_id, report_text, status, category_id) VALUES
(1, 'My maize leaves have holes and worms.', 'pending', 1),
(2, 'Tomatoes are wilting and changing color.', 'pending', 2);

-- ESCALATIONS
INSERT INTO escalations (report_id, escalated_to, reason, status) VALUES
(1, 'County Officer - Kiambu', 'Possible Fall Armyworm outbreak', 'open');

-- KNOWLEDGE BASE
INSERT INTO knowledge_base (title, body, category, created_by) VALUES
('Dealing with Armyworms', 'Spray with approved pesticide every 7 days.', 'Pest Control', 1),
('Post-Harvest Storage Tips', 'Keep grains dry and stored in airtight bags.', 'Harvest', 2);

-- FEEDBACK
INSERT INTO feedback (farmer_id, type, reference_id, feedback_text, rating) VALUES
(1, 'report', 1, 'Thank you, the extension officer responded.', 5),
(2, 'alert', 1, 'I did not receive any rain.', 2);

-- GROUPS
INSERT INTO groups (name, type) VALUES
('Kiambu Farmers', 'region'),
('Maize Growers', 'crop');

-- GROUP MEMBERS
INSERT INTO group_members (group_id, farmer_id) VALUES
(1, 1),
(1, 2),
(2, 1),
(2, 3);

-- CONTENT TRANSLATIONS
INSERT INTO content_translations (content_type, reference_id, language_code, translated_title, translated_body) VALUES
('alert', 1, 'sw', 'Onyo la Mvua Kubwa', 'Mvua kubwa inatarajiwa. Vuna mazao mapema.'),
('knowledge', 1, 'sw', 'Kudhibiti Viwavi', 'Nyunyizia dawa kila siku saba.');

-- MESSAGE LOGS
INSERT INTO message_logs (message_type, recipient_phone, content, status, sent_at) VALUES
('sms', '+254700111222', 'Heavy rain expected. Harvest early.', 'sent', NOW()),
('sms', '+254711222333', 'Heavy rain expected. Harvest early.', 'sent', NOW()),
('sms', '+254722333444', 'Pest alert: check for signs on maize.', 'queued', NULL);

```
## ✅ Approval Request

This project aligns with our mission to empower farmers with practical tools using accessible technology. We seek your approval to begin development with a phased rollout. All code will follow best practices, and documentation will be provided.

