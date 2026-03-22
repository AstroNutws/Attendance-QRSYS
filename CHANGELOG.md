# 🛡️ QrSys: Attendance & Management System
**Modern QR-based attendance tracking for Windows and Android.**
QrSys is a high-performance system designed for organizations to manage attendance, student records, and real-time notifications. Version 2.1.7 marks the transition to a premium "Glassmorphism" aesthetic, aligning both the mobile and desktop experiences with modern design standards.

---

## 🚀 Changelog

### [2.1.7] - The "Seamless Aesthetics" Update - 2026-03-21

#### **PC (Windows) Desktop Enhancements**
- **Global Announcement Hub:** Overhauled the dashboard bulletin from a single "Latest" view to a full-access "Global Announcement" feed.
- **Infinite Scroll Bulletin:** Implemented an `AutoScroll` enabled announcement panel allowing users to view the entire history of updates.
- **Visual Block Separation:** Redesigned the announcement feed with high-contrast separators (`━━━━━━━━`) and emoji-coded headers for better scannability.
- **Unified Brand Identity:** Updated the Taskbar and Form icons to match the new `Qrsys Circle` branding, ensuring a native and professional feel on Windows.
- **Live Clock Optimization:** Improved `Timer1` tick logic for lag-free real-time tracking on the main dashboard.

#### **Mobile (Android) UI & Branding Overhaul**
- **Branded Splash Screen:** Replaced default assets with the official Maroon (#800000) splash branding.
- **Custom Adaptive Icon:** Implemented `Qrsys Circle.svg` as the official app icon for a consistent Android home screen presence.
- **Transparent Status Bar:** Modernized the interface by removing the legacy status bar, allowing Maroon headers and "Glass" cards to flow seamlessly to the top of the display.
- **Glassmorphism UI:** Introduced semi-transparent card layouts with soft-glow maroon shadows for depth and hierarchy.
- **Floating Navigation:** Updated bottom navigation bar with rounded top corners and subtle shadows to mimic a floating dock.

#### **Security Patch — BCrypt Password Hashing (PC & Mobile)**
- **Industry-Standard Hashing:** All passwords are now hashed using `BCrypt.Net-Next` (work factor 11) before being stored in the database. Plain-text password storage has been fully eliminated across all account types.
- **Secure User Registration (PC & Mobile):** Both `register.vb` (Windows) and `RegisterPage.xaml.cs` (Android) now hash passwords with `BCrypt.Net.BCrypt.HashPassword()` before inserting into the `users` table.
- **Secure Admin Registration:** `cregister.vb` now hashes admin passwords with BCrypt before inserting into `admin_accounts`, ensuring no plain-text credentials are ever written to the database.
- **Secure Login Verification (PC & Mobile):** All login flows — user, admin, and super admin — now fetch the stored hash by username only and verify using `BCrypt.Net.BCrypt.Verify()` in application code. Password comparisons have been removed from SQL queries entirely.
- **Developer Account Removed from Login:** Removed the hardcoded developer master account check from `Form1.vb` and `LoginPage.xaml.cs` to eliminate a privileged backdoor from production builds.
- **Database Column Widened:** The `password` column in both `users` and `admin_accounts` tables has been altered from `VARCHAR(50)` to `VARCHAR(72)` to accommodate the 60-character BCrypt hash format.
- **Registration Email Overhaul (Mobile):** Replaced the misused attendance email template for registration with a dedicated `EnqueueRegistrationEmail()` method in `EmailService.cs`, matching the QrSys maroon card template with a green `✓ Registered` badge, Day, Date Registered, Time Registered, and a parent-facing note about QR code generation.

---

### [2.1.6] - The "Peace of Mind" Update - 2026-03-17

#### Added
- **Automatic Security Shield:** The app now automatically checks for and installs security updates.
- **Easy Password Recovery:** Request a password reset directly from the login screen.
- **Admin Help on the Go:** Admins can approve requests and update details via mobile.

#### Fixed
- **Login "Disposed Object" Error:** Fixed the bug causing unexpected app closures during authentication.
- **Faster Connection Loading:** Optimized database handshakes for quicker screen transitions.

---

### [2.1.5] - Better Tracking & Branding - 2026-03-15
- **Smart Attendance Labels:** Implemented **(O)** for out, **(E)** for early exit, and **(L)** for late.
- **Official Maroon Theme:** Migrated all UI elements from purple to the official Maroon and White colorway.

---

## 🛠️ Technical Stack
- **Frontend:** .NET MAUI (Android), VB.NET (Windows Desktop)
- **Backend:** Npgsql (PostgreSQL), SQL Server
- **Tools:** Adobe Photoshop (UI/UX Design), ZXing.Net (QR Processing)
- **Features:** Glassmorphism, Real-time SMTP Notifications, Adaptive Security Updates, BCrypt Password Hashing

---

## 👨‍💻 Developer
**Gabriel** (AstroNutws)
**Contact:** [samongud@gmail.com](mailto:samongud@gmail.com)

---

*Developed with dedication for modern attendance management.*
