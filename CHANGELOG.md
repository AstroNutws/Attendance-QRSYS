# 🛡️ QrSys: Attendance & Management System
**Modern QR-based attendance tracking for Windows and Android.**
QrSys is a high-performance system designed for organizations to manage attendance, member records, and real-time notifications. Version 2.1.7 delivers a sweeping visual overhaul on mobile alongside critical security hardening across both platforms.

---

## 🚀 Changelog

### [2.1.7] - The "Glass & Guard" Update - 2026-03-23

> A dual-front release combining a premium Glassmorphism visual identity on Android with a comprehensive security hardening pass across the entire QrSys infrastructure.

#### 🎨 PC (Windows) — Desktop Experience
- **Global Announcement Hub:** Overhauled the dashboard bulletin from a single "Latest" view to a full-access global feed, giving users visibility over the entire announcement history.
- **Infinite Scroll Bulletin:** Introduced an `AutoScroll`-enabled announcement panel for seamless, uninterrupted reading of all system updates.
- **Visual Block Separation:** Redesigned the announcement feed with high-contrast separators (`━━━━━━━━`) and emoji-coded section headers for faster scannability.
- **Unified Brand Identity:** Updated all Taskbar and Form icons to the new `Qrsys Circle` mark, establishing a consistent and professional native Windows presence.
- **Live Clock Optimization:** Refined `Timer1` tick logic for lag-free, real-time clock rendering on the main dashboard.

#### 📱 Mobile (Android) — UI & Branding Overhaul
- **Branded Splash Screen:** Replaced all default launch assets with the official Maroon (`#800000`) splash identity for an immediately on-brand first impression.
- **Custom Adaptive Icon:** Deployed `Qrsys Circle.svg` as the official adaptive app icon, ensuring a sharp and consistent presence across all Android launcher environments.
- **Transparent Status Bar:** Eliminated the legacy opaque status bar, allowing the Maroon header and Glass cards to extend edge-to-edge for a fully immersive display.
- **Glassmorphism UI:** Introduced a system-wide semi-transparent card design language with soft maroon-glow shadows, creating clear visual hierarchy and modern depth.
- **Floating Navigation Bar:** Redesigned the bottom navigation with rounded corners and layered shadows to achieve a floating dock aesthetic consistent with the new glass design language.

#### 🔒 Security & Stability — Cross-Platform Hardening
- **Credential Protection Overhaul:** Fundamentally strengthened how credentials are stored and verified across all account types on both platforms, bringing the system in line with current industry standards.
- **Login Flow Hardening:** Rearchitected all authentication flows — standard user, admin, and super admin — to follow secure, best-practice verification patterns.
- **Admin Credential Enforcement:** Upgraded the admin account creation system to enforce secure credential policies at the point of registration, closing a prior gap in write-time protection.
- **Production Build Cleanup:** Removed all internal development access points and privileged backdoors from production builds on both PC and mobile, reducing the attack surface of released builds.
- **Database Schema Hardening:** Updated relevant credential storage columns to fully support the new secure format, ensuring schema-level compatibility and integrity.
- **Registration Email Overhaul (Mobile):** Replaced the repurposed attendance notification template for new registrations with a purpose-built branded confirmation email — maroon card layout, registration-specific content, and a parent-facing note regarding QR code generation.

---

### [2.1.6] - The "Peace of Mind" Update - 2026-03-17

#### ✅ Added
- **Automatic Security Shield:** The system now silently checks for and applies critical security updates on launch, ensuring deployments are always on a protected build.
- **Easy Password Recovery:** Users can now initiate a password reset directly from the login screen without administrator intervention.
- **Admin Help on the Go:** Administrators can review, approve, and action requests from the mobile client, enabling remote management without desktop access.

#### 🔧 Fixed
- **Login "Disposed Object" Error:** Resolved a race condition causing unexpected application closures during the authentication sequence.
- **Faster Connection Loading:** Optimized the database handshake process, resulting in noticeably quicker transitions between screens on both platforms.

---

### [2.1.5] - Better Tracking & Branding - 2026-03-15
- **Smart Attendance Labels:** Introduced structured status codes — **(O)** Time Out, **(E)** Early Exit, **(L)** Late Arrival — for clearer and more actionable attendance records.
- **Official Maroon Theme:** Completed a full UI migration from the legacy purple palette to the official Maroon (`#800000`) and White brand colorway across all screens and components.

---

## 🛠️ Technical Stack
- **Frontend:** .NET MAUI (Android), VB.NET (Windows Desktop)
- **Backend:** Npgsql (PostgreSQL), SQL Server
- **Tools:** Adobe Photoshop (UI/UX Design), ZXing.Net (QR Processing)
- **Features:** Glassmorphism, Real-time SMTP Notifications, Adaptive Security Updates, Secure Credential Management

---

## 👨‍💻 Developer
**Gabriel** (AstroNutws)
**Contact:** [samongud@gmail.com](mailto:samongud@gmail.com)

---

*Developed with dedication for modern attendance management.*
