# Requirement Analysis

## Functional Requirements

### FR-1 Book Management
- Librarians can add, update, delete, and search books within the repository
- Every book record contains: Title, Author, Category, Publisher, ISBN, Availability status, Publication details
- Librarians can maintain and modify the active inventory of available books

### FR-2 Member Management
- Maintains complete member profiles
- Each member record includes: Member ID, Member Name, Email Address, Mobile Number, Department, Membership Date

### FR-3 Book Issue Management
- Librarians can issue books to active, registered members
- Each issue transaction stores: Member Name, Book Name, Issue Date, Due Date, Return Date, Status

### FR-4 Fine Management
- Calculates, records, and maintains overdue fee details
- Tracks: Fine ID, Member Name, Book Name, Fine Amount, Fine Status, Payment Date

## Non-Functional Requirements

| Requirement | Description |
|---|---|
| **Performance** | Fast record retrieval even with large concurrent data volumes |
| **Security** | User authentication, custom application roles, and ACLs |
| **Reliability** | Consistent data with no loss during CRUD operations |
| **Scalability** | Supports future barcode/QR scanning, Email/SMS, online reservations |

## Software & Hardware Requirements

**Software**

| Component | Purpose |
|---|---|
| ServiceNow Personal Developer Instance | Core scoped application environment and script hosting |
| Web Browser (Chrome, Firefox, Safari) | Accessing ServiceNow Developer Studio |
| Internet Connection | Cloud instance syncing and remote workspace |
| GitHub | Source repository backup, branching, version control |

**Hardware**

| Parameter | Minimum Specification |
|---|---|
| Processor | Intel i3 / AMD Ryzen 3 or higher |
| RAM | 4 GB minimum (8 GB recommended) |
| Storage | 20 GB free disk space |
| Monitor | 1366 × 768 pixels |
