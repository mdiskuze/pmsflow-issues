  # PMS Flow - Public Issue Tracker

  This repository is the public issue tracker for **PMS Flow**.

  ## Purpose

  Use this repository to:

  - report bugs
  - suggest improvements
  - request new features
  - share usability feedback

  This repository does **not** contain the application source code.

  ## Before You Open an Issue

  Please check existing issues first to avoid duplicates.

  When reporting a bug, include:

  - App version (for example: `1.1.2`)
  - Device model
  - Android version
  - Steps to reproduce
  - Expected behavior
  - Actual behavior
  - Screenshot/video (if possible)

  ## Feature Requests

  Please describe:

  - the problem you are trying to solve
  - your proposed solution
  - why it would be useful in real-life use

  ## Privacy Notice

  Do not post personal or sensitive data (health details, names, emails, phone numbers, exported records).

  ## Security

  If you found a potential security/privacy vulnerability, please **do not** post it publicly in Issues.
  Contact the maintainer privately.

# PMS Flow - App Guide 🌸

Welcome to **PMS Flow**, an app for tracking menstrual cycles, symptoms, predictions, and statistics.

Meaning of `PMS` in the app branding:
- **EN:** `Period Management System`
- **CZ:** `Parťačka Měsíčního Sledování`

---

## 📱 Features

### 🧭 Navigation
- Primary sections are available directly from the bottom bar:
  - Calendar
  - Statistics
  - Shared
  - Backup
  - How-to
- On larger screens (sw600dp+), the app uses a left Navigation Rail for the same primary sections.
- The side drawer is kept for secondary items (Settings, About).

### 🗓️ Calendar
- Color-coded day types:
  - 🔴 **Menstruation**
  - 🩷 **Predicted period (light red)**
  - 🟢 **Fertile days**
  - 🔵 **Ovulation**
  - 🟣 **Symptom indicator**
- Tap any day to open day details.
- Long press any calendar day to open day quick actions (start/end/open detail based on context).
- Day-detail actions are shown as clear buttons (unified UX).
- Weekday labels and cycle status text are localized consistently in both main and shared calendars.
- The FAB ➕ allows:
  - "Log period start and end"
  - "Log pregnancy"
- Long press FAB ➕ triggers the fastest quick action for today.

### 🩸 Menstruation
- Log period start with an optional end date.
- Supports the "Ongoing" state (no end date yet).
- Bleeding intensity supports:
  - overall intensity for the record
  - optional per-day override for a specific day
- Calendar shows an intensity indicator directly on period days.

### ✏️ Edit and Delete
- From day detail you can:
  - edit the record
  - edit bleeding intensity for that day
  - add/edit symptoms
  - delete a record
- For multi-day records, you can delete:
  - a single day only
  - or the whole record
- If a day has no period record, edit actions are hidden and only valid actions are shown.

### 🤰 Pregnancy
- You can log pregnancy manually.
- After the first post-pregnancy period is logged, active pregnancy is closed automatically.
- In statistics, the gap is compressed to keep charts comparable.

### 😊 Symptoms
- Track:
  - abdominal pain
  - mood
  - energy
  - notes
- Days with symptoms are marked in the calendar.
- Tapping a day shows the exact stored symptom values.

### 📊 Predictions
- Estimates for next period, ovulation, and fertile window.
- Prediction confidence is shown (LOW/MEDIUM/HIGH).
- Prediction date uses standard local format (e.g. `5. 4. 2026`).
- Ovulation/fertile calculation is aligned consistently across prediction modes.
- Fertile-window behavior can be configured in Settings:
  - **Standard (6 days):** 5 days before ovulation + ovulation day
  - **Conservative (wider):** wider uncertainty window for variable cycles
- **Gradual fertility** only changes color intensity, not the number of marked days.
- Gradual fertility tint is rendered as a smooth progression (lighter to darker) toward peak fertility.

### 🔔 Notifications
- Period reminders
- Symptom reminders
- Fertile window reminders
- Late-period reminder:
  - after 7 days late
  - once per expected cycle
  - separately toggleable in settings

### 🔐 App Lock
- Optional app lock can be enabled in **Settings > Security**.
- Supported unlock methods:
  - Biometric authentication
  - PIN (4+ digits)
- When enabled, app unlock is required after returning from background.

### 💾 Backup and Restore
- Personal backup/restore for **CSV** and **JSON** is in **Backup**.
- Useful for backup or further analysis.

### 🤝 Local Sharing (Read-Only)
- In **Shared**, you can export/import **Share snapshot (.pmsshare)** for partner/family use.
- Share options:
  - optional profile alias
  - include/exclude symptoms
  - include/exclude notes
- Import `.pmsshare` creates a **read-only shared profile** (separate from your own records).
- Shared entries can be:
  - opened in read-only month calendar
  - renamed locally
  - assigned relationship label (partner/daughter/family/other)
  - filtered in list
  - sorted (updated/name/relationship)
  - deleted locally
- Shared profile cards display `last sync`.
- Optional behavior in Shared Profiles: keep snapshot history instead of overwriting by sender.
- `.pmsshare` can be opened directly in PMS from Android share/file apps (when PMS is selected as target).
- Full practical flow guide (EN): `SHARING_GUIDE.md`
- Full practical flow guide (CS): `SHARING_GUIDE_CS.md`

---

## 🎨 Color Guide

### Calendar
- 🔴 Menstruation
- 🩷 Predicted period (light red)
- 🟢 Fertile days
- 🔵 Ovulation
- 🟣 Symptoms

### Charts and Statistics
- Trends for cycle length, period length, and symptoms.
- Time-range filter: 3 / 6 / 12 months / all.

---

## ⚙️ Technical Info

- **Minimum Android:** 8.0 (API 26)
- Data is stored locally (Room DB)
- Export uses Android system sharing

---

## 🔒 Privacy

- Data stays locally on the device
- The app is not a medical device
- Predictions are estimates based on historical data

---

## 🧾 Versioning

- **App version:** managed via `gradle.properties` (`APP_VERSION_NAME` / `APP_VERSION_CODE`)
<!-- release:auto:start -->
- **Current release:** `1.1.11`
- **Last update:** `2026-02-23`
- **Release source:** `app/CHANGELOG.md`
- **Generated latest metadata:** `release/latest_release.json`
- **Generated GitHub release body:** `release/github_release_body.md`
- **Generate command:** `./scripts/release_prepare.sh`
<!-- release:auto:end -->
- **Change history:** see `CHANGELOG.md`
