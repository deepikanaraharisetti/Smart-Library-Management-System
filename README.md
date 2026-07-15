# Smart Library Management System

The Smart Library Management System is a web-based application built on the **ServiceNow** low-code platform to automate and simplify library management activities — book records, member management, book issue/return tracking, fine calculation, and reporting.

> ⚠️ **This repository is actively connected to a ServiceNow instance via Source Control.**
> The files at the repository root (`sys_remote_update_set_*.xml`, `sn_source_control.properties`, and the hash-named application folder) are **auto-managed by ServiceNow** — they update automatically every time an update set is committed in Studio. Do not manually edit, move, or delete them.

## 📁 Documentation

All project documentation, write-ups, and reference material live in [`docs/`](./docs), organized by phase:

```
docs/
├── 1. Brainstorming & Ideation/
├── 2. Requirement Analysis/
├── 3. Project Design Phase/
├── 4. Project Planning Phase/
├── 5. Project Development Phase/
├── 6. Project Testing/
├── 7. Project Documentation/   ← full PDF report
└── 8. Project Demonstration/
```

See [`docs/README-full.md`](./docs/README-full.md) for the complete project overview (objectives, architecture, ER diagram, roles, setup instructions, and conclusion).

## Quick Links

- 📄 [Full Documentation PDF](./docs/7.%20Project%20Documentation/Smart_Library_Management_System_Final_Documentation.pdf)
- 🧩 [System Design & ER Diagram](./docs/3.%20Project%20Design%20Phase/System-Design.md)
- ⚙️ [Implementation Details](./docs/5.%20Project%20Development%20Phase/Implementation.md)
- ✅ [Testing & Results](./docs/6.%20Project%20Testing/Testing-and-Results.md)

## How to Get the Application

The Library Management scoped application is synced automatically from ServiceNow to this repo's root via the update set XML. To install it on another instance:

1. Copy `sys_remote_update_set_*.xml` from this repo's root
2. In your target ServiceNow instance, go to **System Update Sets → Retrieved Update Sets → Import Update Set from XML**
3. Upload the file, then **Preview** and **Commit**
