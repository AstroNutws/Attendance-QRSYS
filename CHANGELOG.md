# Changelog

All notable changes to the QRSYS project are documented here.

## [2.1.5] - PC & Mobile Ecosystem - 2026-03-15
### Added
- **Smart Checkout Tracking:** Introduced intelligent status recognition. The system now accurately distinguishes between a standard check-out (**O**), "Out Early" (**O(E)**), and "Out Late-In" (**O(L)**) for more precise attendance records.
- **Comprehensive Time Logging:** Attendance dashboards and student logs now display both **"Time In"** and **"Time Out"** simultaneously, providing a complete picture of the school day at a glance.
- **Enhanced Visual Cues:** Added distinct, professional color-coding for the new attendance statuses across both PC and Mobile platforms, making it easier for admins to spot irregularities visually.
- **Parent Registration Alerts:** The system now automatically sends a "Registration Successful" email to parents immediately after a new student account is created, confirming their contact details are linked.
- **Maroon Branding Overhaul:** Replaced the default .NET violet theme with the official QrSys Maroon and White color scheme across the entire mobile application, including the top navigation bars and startup screens.

### Improved
- **Unified Cross-Platform Login:** Synchronized the authentication engine between the PC and Mobile apps. Users can now expect a seamless, identical login experience regardless of which device they use.
- **Search Capabilities:** Upgraded the Mobile Student Finder to load up to 60 recent logs instantly and display precise session durations (e.g., 08:00 AM - 04:00 PM) directly in the search results.
- **Mobile Visual Polish:** Standardized the appearance of the bottom navigation tabs and status bars to match the dark, professional aesthetic of the Admin Hub.

### Fixed
- **Theme Consistency:** Eliminated the "Violet Bar" issue on mobile devices, ensuring a consistent brand experience from the moment the app opens.
- **Account Security:** Fixed a login routing issue where admin and student dashboards could occasionally cross over during the sign-in process.
- **Data Reliability:** Patched a database formatting bug to ensure trailing spaces in user data no longer cause "Unknown" status errors.

---

## [2.1.1] - PC Version - 2026-03-14
### Added
- **Security Update:** Transitioned from Full Name login to a more secure **Username-based authentication**.
- **Communications:** Integrated an **Announcements Dashboard** for broadcasting school-wide information.
- **Data Visualization:** Added a dynamic **Statistics Graph** in the Admin Panel to track attendance trends.
- **Reporting:** Implemented a **CSV Export** feature, allowing admins to download daily attendance logs for external record-keeping.
- **Parental Notifications:** Automatic **Email Alerts** are now sent to parents/guardians the moment a student's QR code is successfully scanned.
- **Smart Filtering:** Enhanced the UI with **Conditional Logic**—selecting a specific Grade Level now dynamically filters and displays only the corresponding Sections.

### Improved
- Complete UI overhaul for a cleaner, modern professional look.
- Optimized database sync speed for high-traffic scanning periods.
- General stability patches and minor bug fixes for the v2.1.x branch.

---

## [2.1.1] - Mobile Client - 2026-03-14
### Added
- **Real-time Sync:** Enhanced mobile-to-cloud synchronization for the scanner module.
- **UI Consistency:** Updated theme colors and button layouts to match the new PC Version branding.
- **Validation:** Added haptic feedback and sound cues for successful scans to ensure the user knows when data is sent.

### Fixed
- Improved camera autofocus for faster QR detection on mid-range Android devices.
- Resolved session timeout issues during long periods of inactivity.
- Synchronized versioning core with the PC edition for ecosystem stability.

---
**Developer:** AstroNutws  
**Contact:** samongud@gmail.com
