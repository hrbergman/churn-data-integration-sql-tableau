### Competitive Churn Analysis - PostgreSQL Data Integration & Tableau Dashboard
**Tools: PostgreSQL, SQL, pgAdmin, Tableau** | M.S. Data Analytics Project (D211 - Advanced Data Acquisition)

This project rebuilt a competitive churn analysis entirely inside a relational database. I loaded a public competitor dataset alongside an internal customer database, reconciled the two schemas in SQL, and fed a single consolidated table into an interactive Tableau dashboard.
 
- Created a new PostgreSQL table for the external dataset and imported it from CSV, then wrote SQL transformations to map text categories (contract type, payment method) to the internal database's reference IDs
- Harmonized field definitions across sources, converting ages to a senior citizen flag, child counts to a dependents indicator, and marital status to a partnership flag so both datasets measured the same things
- Tagged every record with its data source before merging with UNION ALL, preserving lineage so any metric could be traced back to its origin
- Deliberately kept the external table out of the database's foreign-key relationships because its records could not be verified against internal keys, and documented that decision as a known limitation
- Explained how existing foreign-key constraints enforced referential integrity across the contract, payment, job, and location tables

[Documentation](https://github.com/hrbergman/churn-data-integration-sql-tableau/blob/main/churn-data-integration-sql-tableau/churn-analysis-documentation.pdf)
| 
[Video Presentation](https://youtu.be/9utEBRqidYk)
