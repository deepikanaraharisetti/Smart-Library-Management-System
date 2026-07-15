# System Design

## System Architecture

The system follows a layered architecture:

- **User Layer** — Administrators, Librarians, Students accessing via web interface
- **Application Layer** — Business Rules, Client Scripts, UI Policies, Flow Designer, Reports, Dashboards
- **Database Layer** — Relational tables (Books, Members, Book Issue, Fine) connected via reference fields
- **Security Layer** — User Authentication, Roles, and Access Control Lists (ACLs)

## Entity Relationship Design

```
Books      → Referenced by → Book Issue ← Referenced by ← Members
Book Issue → Referenced by → Fine
```

### Table Schemas

**Books**
- book_id (PK, INT)
- book_name (VARCHAR)
- author (VARCHAR)
- category (VARCHAR)
- publisher (VARCHAR)
- isbn (VARCHAR)
- available (BOOLEAN)
- description (TEXT)

**Members**
- member_id (PK, INT)
- member_name (VARCHAR)
- email (VARCHAR)
- phone_number (VARCHAR)
- department (VARCHAR)
- membership_date (DATE)

**Book Issue**
- issue_id (PK, INT)
- book_id (FK)
- member_id (FK)
- issue_date (DATE)
- due_date (DATE)
- return_date (DATE)
- status (VARCHAR)

**Fine**
- fine_id (PK, INT)
- issue_id (FK)
- member_id (FK)
- fine_amount (DECIMAL 10,2)
- fine_status (VARCHAR)
- remarks (TEXT)
