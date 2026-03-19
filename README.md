<div align="center">

<h1>Software Consultancy Database</h1>
<p><em>Oracle SQL schema for customers, projects, consultations, assets, billing, and access control.</em></p>

</div>

## 📂 What’s inside
- `schema.sql` – full DDL/DML + sample reports and role grants.
- Example queries: filtering, grouping, joins, ordering.
- PL/SQL: CRUD procedures, reporting cursors, discount calculator.

## 🚀 Quickstart (Oracle)
1. Connect as a user with `CREATE USER` and `CREATE ROLE` privileges.
2. Run the script:
   ```sql
   @schema.sql
   ```
3. Verify sample data:
   ```sql
   SELECT * FROM customer;
   SELECT * FROM consultation;
   ```

## 🔍 Highlights
- Identity columns for primary keys (Oracle 12c+).
- Check constraints on phone length, asset price, and quantity.
- Foreign keys across customers, projects, consultations, tasks, orders, invoices, and payments.
- Roles & users: `admin_role`, `developer_role`, `client_role` with least-privilege grants.

## 🧰 PL/SQL Toolkit
- `AddCustomer`, `ReadCustomer`, `UpdateCustomer`
- `ScheduleConsultation`, `UpdateConsultationStatus`
- `GetProjectConsultations` (REF cursor)
- `GetCustomerStats` (client activity)
- `CalculateAssetDiscount`
- Reports: `ClientActivityReport`, `DigitalAssetReport`, `DeveloperPerformanceReport`

## 📑 Usage tips
- Update sample emails/phones to match your locale rules if needed.
- Adjust hourly rates and currency in `ProjectTask` to your billing model.
- Replace sample users/passwords before production.
- Wrap DML in transactions if you extend the script for migrations.


---
