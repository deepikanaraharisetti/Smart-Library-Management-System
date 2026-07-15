# Implementation

## Overview

The application was built as a secure **Scoped Application** inside ServiceNow Studio. All data schemas, access controls, automated business workflows, and user views were compiled into this independent namespace.

## Modules

- **Books** — book inventory (Book ID, Title, Author, Category, ISBN, Total Copies, Availability)
- **Members** — member registration (Member ID, Name, Email, Phone Number, Department, Join Date, Status)
- **Book Issue** — issue/return transactions (Issue ID, Book, Member, Issue Date, Due Date, Return Date, Status)
- **Fine Table** — fine records (Fine ID, Book Issue, Fine Amount, Paid, Payment Date)

## Business Rules (Server-Side Automation)

Business Rules handle backend data integrity:

- **Book Available on Return** — sets availability flag to `true` when a book is returned
- **Book Unavailable on Issue** — sets availability flag to `false` when a book is issued
- **Prevent Duplicate Book Issue** — blocks issuing a copy that's already checked out

## Client Scripts & UI Policies (Client-Side Validation)

UI Policies dynamically control form field behavior without heavy scripting:

| Table | Field | Policy | Read-only | Mandatory | Visible |
|---|---|---|---|---|---|
| Book Issue | book | Book read only | true | false | true |
| Fine Table | fine_amount | Show fine amount | false | false | true |
| Book Issue | return_date | Return date mandatory | false | true | true |

## Role-Based Access Control (ACLs)

- **Administrator** — master rights: infrastructure, access policies, table mappings
- **Librarian** — full CRUD on transaction records for daily operations
- **Student** — read-only: search books, check issued books and fine status

ACLs are enforced per table (Books, Book Issue, Fine Table) across `read`, `write`, `create`, and `delete` operations.
