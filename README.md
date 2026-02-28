# EPL 2021-2022 Data Warehouse Project

## Project Overview

A collaborative data warehouse built as part of an Advanced Database course, analyzing the English Premier League 2021-2022 season. Features automated ETL pipeline execution, star schema design, and SCD Type 6 implementation for historical player tracking.

### Data Source
[Kaggle - EPL 21-22 Matches & Players](https://www.kaggle.com/datasets/azminetoushikwasi/epl-21-22-matches-players)

## Team Contributions

This was a collaborative effort with clearly defined responsibilities:

| Team Member | Contribution |
|------------|--------------|
| **Basmala** | Star Schema Design - Designed dimension and fact table structures, defined relationships and keys |
| **Malak** | ETL & SendMail SP - Implemented data transformation logic and automated email notifications |
| **Laila** | Source ERD, SCD Type 6, Fact Loading - Created source data model, built SCD procedure, and implemented fact loading logic |
| **Jumanah (me)** | Pipeline Automation - Designed and built the automated execution system using batch scripting and Windows Task Scheduler |

## My Contribution

**Role**: Pipeline Automation

I built the **automated scheduling** for the data warehouse, enabling daily ETL execution without manual intervention.

### Responsibilities:
- **Batch Script Development**: Created Windows batch file to execute the ETL pipeline via sqlcmd
- **Task Scheduling**: Configured Windows Task Scheduler for daily execution at 1:00 PM to ensure fresh data availability
- **Pipeline Automation**: Automated the execution of the ETL workflow which includes:
  1. Connecting to SQL Server instance
  2. Executing main ETL procedure
  3. Loading staging tables from CSV files
  4. Updating dimension and fact tables
  5. Triggering email notifications

## Project Structure

```
EPL-data-warehouse/
├── README.md
│
├── database-schema/
│   ├── Football_DW_Analytics_Queries.sql
│   ├── Staging_Tables.sql
│   └── StarSchema.sql
│
├── job-automation/
│   ├── runJob.bat
│   └── runProcedure.sql
│
├── matchdata/
│   ├── all_match_results.csv
│   ├── all_players_stats.csv
│   └── points_table.csv
│
└── stored-procedures/
    ├── ETL_Main_Procedure.sql
    ├── Fact_Procedure.sql
    └── SCD_Procedure.sql
```

