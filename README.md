# Smart Library Management System

## Project Overview

The Smart Library Management System is a web-based application built on the **ServiceNow** low-code platform to automate and simplify library management activities. It provides a centralized platform for maintaining book records, managing library members, issuing and returning books, calculating fines, and generating reports — replacing manual, register-based library operations with a secure, efficient digital solution.

---

## Objective

The objective of this project is to eliminate manual, paper-based library workflows by providing:

- Centralized digital records for books and members
- Automated book issue and return tracking
- Automated fine calculation
- Role-based secure access (Administrator, Librarian, Student)
- Analytical reports and dashboards for decision-making

---

## Features

- Scoped Application built entirely on ServiceNow
- Book, Member, Book Issue, and Fine management modules
- Business Rules for server-side automation (availability flags, duplicate-issue prevention)
- Client Scripts and UI Policies for dynamic, validated forms
- Role-based Access Control Lists (ACLs) for Admin / Librarian / Student
- Reports and interactive dashboards for library analytics

---

## Technologies Used

### Platform
- ServiceNow (Personal Developer Instance / Scoped Application)

### Core Components
- Business Rules (server-side automation)
- Client Scripts (client-side validation)
- UI Policies (dynamic form behavior)
- Access Control Lists (ACLs)
- Reports & Performance Analytics Dashboards

### Development Tools
- ServiceNow Studio
- Web Browser (Chrome / Firefox / Safari)
- Git & GitHub (source control / update set sync)

---

## Project Structure

```
Smart-Library-Management-System/
│
├── 1. Brainstorming & Ideation/
│   └── Problem-Statement-and-Ideation.md
│
├── 2. Requirement Analysis/
│   └── Requirement-Analysis.md
│
├── 3. Project Design Phase/
│   └── System-Design.md
│
├── 4. Project Planning Phase/
│   └── Execution-Roadmap.md
│
├── 5. Project Development Phase/
│   └── Implementation.md
│
├── 6. Project Testing/
│   └── Testing-and-Results.md
│
├── 7. Project Documentation/
│   ├── Smart_Library_Management_System_Final_Documentation.pdf
│   └── sys_remote_update_set_7bd4151647c2c710cbc3392f316d43ea.xml
│
├── 8. Project Demonstration/
│   └── Demo-Notes.md
│
└── README.md
```

---

## Database Design (Entity Relationships)

```
Books      → Referenced by → Book Issue ← Referenced by ← Members
Book Issue → Referenced by → Fine
```

**Tables:**
- **Books** — Book ID, Book Name, Author, Category, Publisher, ISBN, Available, Description
- **Members** — Member ID, Member Name, Email, Phone Number, Department, Membership Date
- **Book Issue** — Issue ID, Book (Reference), Member (Reference), Issue Date, Due Date, Return Date, Status
- **Fine** — Fine ID, Book Issue (Reference), Member (Reference), Fine Amount, Fine Status, Remarks

---

## User Roles

| Role | Access |
|---|---|
| **Administrator** | Master rights — configure access policies, manage core table mappings |
| **Librarian** | Full CRUD on books, members, issues, and fines |
| **Student** | Read-only — search books, view issued books, check fine status |

---

## How to Set Up the Project

### Step 1
Clone the repository
```
git clone https://github.com/deepikanaraharisetti/Smart-Library-Management-System.git
```

### Step 2
Import the update set XML — [`7. Project Documentation/sys_remote_update_set_7bd4151647c2c710cbc3392f316d43ea.xml`](./7.%20Project%20Documentation/sys_remote_update_set_7bd4151647c2c710cbc3392f316d43ea.xml) — into your ServiceNow Personal Developer Instance via **System Update Sets → Retrieved Update Sets → Import Update Set from XML**.

### Step 3
Preview and **Commit** the update set to install the Library Management scoped application.

### Step 4
Assign roles (`x_..._librar_0.Admin`, `x_..._librar_0.Librarian`, `x_..._librar_0.Student`) to your test users.

### Step 5
Open the **Library Management System** application in the ServiceNow Navigator and start managing books, members, issues, and fines.

---

## Future Scope

- Barcode / QR code scanning for book issue and return
- Email and SMS notifications for due dates and fines
- Online book reservation functionality
- Integration with external library databases and APIs

---

## Conclusion

The Smart Library Management System was successfully developed and deployed on the ServiceNow cloud environment. Using platform-native features — Scoped Applications, Business Rules, UI Policies, and custom dashboards — the application automates day-to-day library operations, removes duplicate/manual data entry, secures data transactions, and scales cleanly with institutional growth.

## Full Documentation

See [`7. Project Documentation/Smart_Library_Management_System_Final_Documentation.pdf`](./7.%20Project%20Documentation/Smart_Library_Management_System_Final_Documentation.pdf) for the complete project report.
