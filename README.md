# dataform-bigquery - Dataform / SQLX for BigQuery

This repository contains Dataform SQLX logic to build staging tables in BigQuery based on the raw external table.

## Setup

1. Update `dataform.json` with your `projectId` and `database`.
2. Install the Dataform CLI and dependencies:

```
npm install
```

## Run Dataform

```
dataform run
```

## Contents

- `definitions/stg_employees.sqlx` builds `analytics.stg_employees` from the external raw table `analytics.raw_employees_ext`.
- Column-level protection is configured via BigQuery policy tags in Terraform in repo1.
