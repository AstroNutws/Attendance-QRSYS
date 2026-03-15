# QRSYS | Quick Start Guide

Welcome to the **QRSYS Attendance Logging System**. Follow this guide to properly set up and manage your organization’s attendance infrastructure.

---

## 🎥 Video Walkthroughs

Before beginning the setup, we highly recommend watching these short guides:

* **Desktop Admin Setup:** https://youtu.be/ZcIJaQYzTzw
* **Mobile Scanner Guide:** https://streamable.com/a4n7ic

---

## 🛠 Hardware Requirements

To ensure the fastest scanning speeds and reliable notifications, ensure your hardware meets these standards:

* **Admin PC:** Windows 7 to 11 with at least 4GB RAM.
* **Scanning Camera:** 720p (HD) Webcam or better to prevent "motion blur" during rapid scanning.
* **Mobile Device:** Android 8.0+ with a functioning **Autofocus** camera.
* **Internet:** A stable connection is required for cloud synchronization and email alerts.

---

## 1. Initial Desktop Setup

1. **Organization Selection:** Upon launching the system, select your institution (e.g., Divine Mercy College Foundation Inc) from the "Select Organization" dropdown to link to your specific cloud database.
2. **Login:** Log in using your authorized **Username**. (Note: Full Name login has been deprecated for security).
3. **Database Sync:** Ensure the "Cloud Sync Status" in the bottom corner shows **VERIFIED**.
4. **Announcement Setup:** Use the **Announcements Dashboard** to post school-wide alerts; these will be visible to staff during the scanning process.

## 2. Managing Student Data

The system uses smart filtering to reduce data entry errors:

* **Grade & Section:** Select the **Grade Level** first. The system will automatically filter the **Section** list to show only relevant options for that grade.
* **Parent Emails:** Ensure every student profile has a valid parent/guardian email address. This is required for the **Instant Email Notification** feature.

## 3. The Scanning Process

### Mobile Client (v1.9.0)
* **Positioning:** Hold the device 4–6 inches away from the QR code.
* **Feedback:** Listen for the **Success Tone** and feel for the haptic vibration. This confirms the data has successfully reached the cloud.
* **Autofocus:** If the scan is blurry, tap the center of the screen to trigger high-speed autofocus.

### PC Client
* If using a webcam for scanning, ensure the scanning area is well-lit to prevent resolution errors.

## 4. Reports & Analytics

* **Real-time Graphs:** View the **Daily Attendance Graph** in the Admin Panel to see peak arrival and departure times at a glance.
* **Exporting Logs:** To generate a hard copy or Excel-ready file, click **Export to CSV**. This will save a spreadsheet of the day's attendance to your local storage.

## 5. Troubleshooting (v2.1.1 Patch Notes)

| Issue | Solution |
| :--- | :--- |
| **"Config Error" (Disposed Object)** | Resolved in v2.1.1. Update your client to fix the `ManualResetEventSlim` access exception during organization selection. |
| **"Green Screen" Error** | Check your webcam connection or reset the resolution in the PC settings. |
| **Email Not Sending** | Verify the school's internet connection and ensure the parent's email is spelled correctly in the database. |
| **Sync Timeout** | Restart the application to refresh the Cloud API handshake. |

---

### Need Further Assistance?

For organizational setup, licensing, or 3-year renewal inquiries, please contact:

**AstroNutws Support** 📧 samongud@gmail.com

---

**Developer:** (AstroNutws)
**Last Updated:** March 14, 2026
