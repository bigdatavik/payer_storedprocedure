# Modernizing Payer Workloads with Databricks SQL Stored Procedures

## Overview

This project demonstrates how to build and manage **Databricks SQL Stored Procedures** to power operational and analytical use cases for payer organizations (such as health insurance or claims processing) on the Databricks Lakehouse platform.

With the recent introduction of SQL stored procedures in Databricks (Public Preview), teams can modularize, reuse, and govern their complex SQL logic natively in the Lakehouse. This streamlines the migration of legacy enterprise data warehouse workloads, simplifies ETL, and enables easily repeatable data management patterns.

## Features

- Example Databricks SQL stored procedures for payer data management and analytics
- Modular business logic (update, cleanse, aggregate, etc.)
- Parameterized procedures governed under Unity Catalog
- Simple calling pattern with `CALL` for orchestrating end-to-end workflows

## Getting Started

### Prerequisites

- Databricks SQL, Databricks Runtime 17.0 and above, Unity Catalog only
- Public Preview access to SQL Stored Procedures
- Sample data/tables for testing

### Usage

1. **Clone this repository:**
   ```bash
   git clone https://github.com/bigdatavik/payer_storedprocedure.git
   ```
2. **Review and customize the stored procedures (SQL files) for your environment and business rules.**
3. **Register your procedures in Unity Catalog:**
   - Use the following command in Databricks SQL:
     ```sql
     CREATE PROCEDURE <catalog>.<schema>.<procedure_name>(<parameters>)
     BEGIN
       -- your logic here
     END;
     ```
4. **Call your procedure as needed:**
   ```sql
   CALL <catalog>.<schema>.<procedure_name>(<arguments>);
   ```

### Example Use Cases

- Data cleaning (e.g., cleansing claims or member information)
- Rule-based updates (e.g., status transitions for claims)
- Aggregations for reporting and analytics
- Migration of legacy stored procedure logic from SQL Server, Oracle, or Teradata

## Why SQL Stored Procedures in Databricks?

- **Consistency & Reusability:** Centralizes complex SQL logic once for repeated, governed use.
- **Governed & Auditable:** Fully managed in Unity Catalog with role-based controls.
- **Migration Friendly:** Move code from enterprise data warehouses with minimal rewrite.
- **Modular Development:** Organize business logic, ETL, and maintenance in callable units using standard SQL.

## Resources

- [Official Databricks Blog: Introducing SQL Stored Procedures in Databricks](https://www.databricks.com/blog/introducing-sql-stored-procedures-databricks)
- [Databricks SQL Documentation](https://docs.databricks.com/en/sql/language-manual/sql-ref-syntax-ddl-create-procedure.html)
- [Public Preview Announcement](https://www.databricks.com/blog/introducing-sql-stored-procedures-databricks)

## License

MIT

***
