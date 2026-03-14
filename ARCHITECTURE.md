# QRSYS Technical Architecture

This document provides a high-level overview of the internal mechanics, data flow, and security protocols of the QRSYS Attendance Logging System.

## 1. The Technology Stack

QRSYS is built using a modern, distributed architecture to ensure low latency and high availability across campus environments.

* **Desktop Client (Admin Panel & Scanner):** Developed in **VB.NET**, optimized for Windows environments. It handles high-speed data processing, administrative reporting, and real-time visualization.
* **Mobile Client (Scanner App):** Built using **.NET MAUI**, providing a native Android experience. It utilizes the device's camera hardware for rapid QR code acquisition and validation.
* **Backend Infrastructure:** Powered by **Supabase (PostgreSQL)**. This provides a relational data structure for complex student-grade-section logic and real-time database listeners.
* **Notification Engine:** A dedicated module that handles SMTP/Cloud API triggers for instant automated email alerts to parents.

## 2. System Workflow & Data Path



The lifecycle of an attendance log follows a strict five-step verification path:

1.  **Ingestion:** The Mobile Client scans the student's unique QR code.
2.  **Logic Validation:** The system applies **Conditional Filtering**, ensuring the student is logged into the correct Grade Level and Section.
3.  **Cloud Synchronization:** Validated logs are pushed to the PostgreSQL database in real-time.
4.  **Automated Alerting:** The system identifies the linked parent/guardian email and dispatches a notification timestamped with the entry/exit event.
5.  **Administrative Audit:** The PC Version pulls the updated data into the **Daily Statistics Graph** and prepares the logs for **CSV Export**.

## 3. Security & Data Integrity

To protect student privacy and ensure system reliability, QRSYS implements the following:

* **Credential Security:** The system has transitioned from name-based access to **Username-based Authentication** for all administrative roles to prevent unauthorized dashboard access.
* **Relational Integrity:** Database schemas are designed with strict foreign key constraints, preventing "orphan" attendance logs and ensuring every scan is tied to a verified student record.
* **Encrypted Transport:** All communication between the PC/Mobile clients and the Supabase backend is conducted over secure, encrypted channels.
* **Access Control:** Administrative privileges are required to access the **Announcement Dashboard** and the **CSV Export** utility.

---
**Developer:** AstroNutws  
**Contact for Technical Inquiries:** samongud@gmail.com
