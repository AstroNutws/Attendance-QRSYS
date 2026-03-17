# Changelog

All notable changes to the QRSYS project are documented here.

## [2.1.6] - System Security Update - 2026-03-17
### Added
- **Updated The System Security:** Forced Auto Update Aswell As A Security Update Inside The app.
## [2.1.5] - Super Admin Ecosystem Update - 2026-03-15
### Added
- **True Super Admin Management:** Upgraded the `super admin panel` to allow management of all administrator accounts, including the promotion and demotion of other Super Admins.
- **Granular Privilege Control:** Integrated a "Super Admin" toggle in both the registration and management forms to define account-level permissions.
- **Safe State Handling:** Implemented `IsDBNull` checks in the management panel to prevent application crashes when encountering legacy accounts with null privilege status.
- **Self-Modification Safety Lock:** Added a logic bridge to prevent Super Admins from accidentally demoting themselves, ensuring at least one Super Admin remains active.
- **Intelligent Admin Change Logs:** Updated the security engine to track exactly what changes are made to administrator accounts, generating a "Before & After" comparison for usernames and emails.
- **Dual-Recipient Security Alerts:** When an administrator's email is updated, the system now automatically notifies both the old and new addresses to prevent unauthorized takeovers.
- **Interactive "Secret" Password Reveal:** Integrated a secure "Click to Reveal" CSS block in security emails, hiding new credentials behind a toggle for better privacy.
- **Smart Checkout Tracking:** Introduced intelligent status recognition. The system now accurately distinguishes between a standard check-out (**O**), "Out Early" (**O(E)**), and "Out Late-In" (**O(L)**).
- **Comprehensive Time Logging:** Dashboards and logs now display both **"Time In"** and **"Time Out"** simultaneously for a complete school day overview.
- **Parent Registration Alerts:** The system now automatically sends a "Registration Successful" email to parents immediately after a student account is linked.
- **Maroon Branding Overhaul:** Replaced the default .NET violet theme with the official QrSys Maroon and White scheme across the entire mobile app.

### Improved
- **Partial Profile Updates:** Refined the Super Admin Panel to allow selective updates (change just password, email, or username) without re-entering all credentials.
- **Unified Cross-Platform Login:** Synchronized the authentication engine between PC and Mobile for an identical, seamless login experience.
- **Search Capabilities:** Upgraded Mobile Student Finder to load 60 recent logs instantly with precise session durations.
- **Developer Support Integration:** Added direct links to the official developer portfolio (`joshuagabriel.me`) within all automated system emails.

### Fixed
- **Cast Exception Patch:** Fixed `System.InvalidCastException` when loading admin lists by implementing robust `DBNull` handling for the `is_superadmin` boolean field.
- **Database Logic Safety:** Implemented fallback logic in the Admin Panel to ensure accidental empty fields no longer overwrite existing records with blank values.
- **Email Delivery Reliability:** Optimized the `ConcurrentQueue` handling in `EmailService` to ensure security alerts are prioritized during high-traffic scanning.
- **Theme Consistency:** Eliminated the "Violet Bar" issue on mobile devices for a consistent brand experience.
- **Account Security:** Fixed a login routing issue where admin and student dashboards could occasionally cross over during sign-in.
- **Data Reliability:** Patched a database formatting bug to ensure trailing spaces no longer cause "Unknown" status errors.

---

## [2.1.1] - PC Version - 2026-03-14
### Added
- **Security Update:** Transitioned from Full Name login to a secure **Username-based authentication**.
- **Communications:** Integrated an **Announcements Dashboard** for broadcasting school-wide information.
- **Data Visualization:** Added a dynamic **Statistics Graph** in the Admin Panel to track attendance trends.
- **Reporting:** Implemented **CSV Export** for downloading daily attendance logs.
- **Parental Notifications:** Automatic **Email Alerts** sent to parents the moment a student's QR code is scanned.
- **Smart Filtering:** Selecting a Grade Level now dynamically filters and displays only corresponding Sections.

---

## [2.1.1] - Mobile Client - 2026-03-14
### Added
- **Real-time Sync:** Enhanced mobile-to-cloud synchronization for the scanner module.
- **UI Consistency:** Updated theme colors and layouts to match the new PC Version branding.
- **Validation:** Added haptic feedback and sound cues for successful scans.

### Fixed
- Improved camera autofocus for faster QR detection on mid-range devices.
- Resolved session timeout issues during inactivity.
- Synchronized versioning core with the PC edition for ecosystem stability.

---
**Developer:** Joshua Gabriel De Leon (AstroNutws)  
**Contact:** samongud@gmail.com
