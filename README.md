# IMSciences Student Database Management System

A Database Management System (DBMS) designed for the **Institute of Management Sciences (IMSciences), Peshawar** to efficiently manage student records, departments, instructors, and courses. The system streamlines data storage, ensures consistency, and supports rich query execution.

## Features

- **Entity-Relationship modeling** of the academic domain
- **Relational schema construction** using both top-down and bottom-up approaches
- **Normalization** up to the 3rd Normal Form (3NF) for optimized storage
- **SQL queries** for common operations (retrieving student data, department info, instructor assignments)
- **Views** for quick, read-only access to common data slices
- **Stored procedures** automating student enrollment, grading, and reporting
- **Functions** for computing averages, counting students, and bulk lookups
- **Triggers** enforcing constraints (course-enrollment limits, prerequisite checks)

## Database schema

Core entities:

| Entity      | Notes |
|-------------|-------|
| Student     | Split into Graduate & Undergraduate sub-types |
| Instructor  | Linked to Department |
| Department  | Owns courses and instructors |
| Course      | Has prerequisites, enrollment limits |
| Room        | Physical location |
| Class       | A scheduled offering of a Course in a Room |
| Enrollment  | Junction between Student and Class with grade |

The full ER diagram, relational schema, normalization steps, and SQL listings are documented in [`database-design.pdf`](database-design.pdf).

## Installation

1. Install **Oracle Database** (or any SQL-compliant DBMS — MySQL, PostgreSQL, SQL Server should also work with minor syntax tweaks).
2. Run the `CREATE TABLE` scripts from the design document in order.
3. Insert sample data (sample `INSERT` statements are provided in the document).
4. Execute the views, stored procedures, functions, and triggers to set up the active behavior.
5. Run the example queries to verify the install.

## Usage

- Manage student records (enrollment, transcripts, department transfers)
- Automate enrollment workflows and grade calculations
- Enforce academic rules with triggers (e.g., a student cannot enroll in a course whose prerequisite they have not passed)

## SQL highlights

- **Stored procedures** — insert new students, enroll in courses, assign grades
- **Triggers** — prevent over-enrollment, enforce prerequisites
- **Functions** — compute course grade averages, count students per department

## Contributing

Pull requests welcome — improvements to queries, new features, or DBMS-specific ports (Postgres / MySQL) are all useful.

## Author

[YasirAfriday](https://github.com/YasirAfriday)
