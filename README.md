<div align="center" style="background-color: #800000; padding: 40px; border-radius: 12px; margin-bottom: 20px;">
  <h1 style="color: #ffffff; margin: 0; font-family: sans-serif;">QRSYS | Attendance Logging</h1>
  <p style="color: #ffffff; font-size: 1.1rem; margin-top: 10px; opacity: 0.9;">Secure Infrastructure for Modern Attendance Logging.</p>
</div>

## Overview
QRSYS is a professional-grade attendance logging system designed specifically for educational institutions. It provides a synchronized infrastructure across desktop and mobile platforms, utilizing QR code scanning to efficiently manage and track attendance.

## Features
- **Dual Platform Integration:** Windows Desktop & Android Mobile.
- **Real-time Synchronization:** Powered by Supabase Cloud.
- **Email Notifier:** Automated alerts to parents/guardians including dedicated registration confirmation emails.
- **Admin Dashboard:** Announcement management and student filtering.
- **Rapid Scanning:** Optimized autofocus for webcam and mobile cameras.
- **Smart Reporting:** Instant CSV exports and daily attendance analytics.

## 🔒 Security & Data Privacy
In compliance with the **Data Privacy Act of 2012 (RA 10173)**, QRSYS is built with a "Security First" approach:

- **BCrypt Password Hashing:** All user, admin, and super admin passwords are hashed using industry-standard BCrypt (`BCrypt.Net-Next`, work factor 11) before storage. Plain-text passwords are never written to the database.
- **SQL Injection Prevention:** Password verification is performed entirely in application code using `BCrypt.Verify()`. No raw password values are passed through SQL queries.
- **Encrypted Transit:** All data sent between the clients (PC/Mobile) and the cloud is encrypted via SSL/TLS.
- **Minimal Data Footprint:** No biometric data (fingerprints/face scans) is stored. The system only tracks the necessary QR Identifier linked to student profiles.
- **Authorized Access:** Management features are locked behind secure admin credentials to prevent unauthorized data exposure.
- **Role-Based Access Control:** Super Admin privileges are enforced at both the application and database level, restricting sensitive operations to authorized accounts only.

## System Requirements

### Desktop Client
- **OS:** Windows 10/11 (x64/x86)
- **Imaging:** USB Webcam (720p+ recommended for speed)
- **Storage:** 400MB Required
- **Network:** Stable Wi-Fi/LAN for Cloud Sync

### Mobile Client
- **OS:** Android 8.0 (Oreo) or higher
- **Hardware:** Camera with Autofocus capability
- **Memory:** 2GB RAM Minimum
- **Capacity:** 50MB Available

## Installation
Download the latest stable builds directly from the GitHub releases page.

- [Desktop PC/Laptop Download](https://github.com/AstroNutws/Attendance-QRSYS/releases/latest)
- [Mobile APK Download](https://github.com/AstroNutws/Attendance-QRSYS/releases/latest)

## Video Walkthroughs
- **Desktop System:** [Watch on YouTube](https://youtu.be/ZcIJaQYzTzw)
- **Mobile App:** [Watch on Streamable](https://streamable.com/a4n7ic)

<br>

<div style="background-color: #ffffff; border: 2px solid #800000; border-radius: 8px; padding: 25px; margin-top: 30px;">
  <h2 style="color: #800000; margin-top: 0; border-bottom: none;">Organizational Deployment</h2>
  <p style="color: #333333; font-size: 1.05rem;">If you want this project for your organization or school, please get in touch to discuss implementation, licensing, and technical setup.</p>
  <p style="font-size: 1.1rem; margin-bottom: 0;">
    <strong>Contact:</strong> <a href="mailto:samongud@gmail.com" style="color: #800000; font-weight: bold; text-decoration: none;">samongud@gmail.com</a>
  </p>
</div>

<br>

---

<div align="center" style="margin-top: 20px;">
  <p style="color: #800000; font-weight: 700; letter-spacing: 1px; text-transform: uppercase; font-size: 0.8rem;">&copy; 2026 QRSYS Academic Infrastructure</p>
</div>
