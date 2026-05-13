![PHP](https://img.shields.io/badge/PHP-7%2B-blue?logo=php)
![Bootstrap](https://img.shields.io/badge/UI-Bootstrap-purple?logo=bootstrap)
![MySQL](https://img.shields.io/badge/Database-MySQL-orange?logo=mysql)
![License](https://img.shields.io/badge/License-MIT-green)

# College Management System (PHP)

A role-based college administration web application built with PHP and MySQL. The system supports three user roles — **Admin**, **Teacher**, and **Student** — and handles the core operations of a college: admissions, academics, attendance, fee management, timetables, and results.

## Features

- **Role-based Access** — separate portals for Admin, Teacher, and Student
- **Admissions Management** — student admission records and application tracking
- **Academics** — course and subject management, timetable scheduling
- **Attendance Tracking** — student and teacher attendance records
- **Fee Management** — student fee assignment and payment tracking
- **Results & Marks** — enter and display student results per class
- **Teacher Management** — salary records, subject assignments, attendance
- **Account Management** — create and manage student/teacher accounts

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Backend | PHP 7+ |
| Database | MySQL |
| Frontend | Bootstrap, CSS |
| Architecture | MVC-style with shared `Common/` includes |
| DB Driver | MySQLi (PHP) |

## Database Schema Overview

The database (`Database/imperial_college.sql`) contains the following key tables:

| Table | Purpose |
|-------|---------|
| `students` | Student profiles and admission data |
| `teachers` | Teacher records and subject assignments |
| `courses` / `subjects` | Academic catalogue |
| `attendance` | Daily attendance for students and teachers |
| `fees` | Fee records per student |
| `results` | Marks and exam results |
| `accounts` | Login credentials for all roles |
| `timetable` | Class scheduling |

> Import `Database/imperial_college.sql` into MySQL before running the app.

## Getting Started

### Prerequisites

- PHP 7+, MySQL 5.7+, Apache (XAMPP / WAMP recommended)

### Installation

```bash
# 1. Clone into your web server's htdocs / www directory
git clone https://github.com/ronikdedhia/College-Management-PHP.git

# 2. Import the database
# Open phpMyAdmin → Create database → Import Database/imperial_college.sql

# 3. Configure DB connection
# Edit Connection/ or config files with your MySQL host, user, password

# 4. Open in browser
http://localhost/College-Management-PHP/
```

### Admin Credentials

> Default admin credentials are seeded in `imperial_college.sql`. Look for the `accounts` table or admin seed rows. **Change credentials before deploying to production.**

## File / Folder Structure

```
College-Management-PHP/
├── index.php                  # Landing page (CHMSC intro)
├── admission.php              # Admission management
├── academics.php              # Academic overview
├── Admin/                     # Admin panel: students, teachers, results, fees
├── Student/                   # Student portal
├── Teacher/                   # Teacher portal
├── Login/                     # login.php, logout.php
├── Common/                    # Shared header, footer, cards
├── Connection/                # DB connection config
├── Database/
│   └── imperial_college.sql   # Full DB schema + seed data
├── Bootstrap/                 # Bootstrap assets
├── Css/ / Images/             # Styling and media
└── composer.json
```

## License

MIT License — see [LICENSE](LICENSE) for details.
