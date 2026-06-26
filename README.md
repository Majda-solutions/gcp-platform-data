# Dataform BigQuery project

This repository holds the Dataform SQLX code for a simple BigQuery transformation.

It contains one transformation that builds a staging table from an existing raw table in BigQuery.

## What this repo does

- Stores the Dataform definitions in the `definitions` folder.
- Uses SQLX files to define the transformation logic.
- Works with GitHub Actions to check the project on pull requests and push to main.

## Local setup

1. Install Node.js.
2. Run:

```bash
npm install
```

3. Compile the project:

```bash
npx @dataform/cli compile
```

## Workflow

The GitHub Actions workflow:

- runs on pull requests to main
- runs on pushes to main
- compiles the Dataform project
- runs the project on pushes to main when the required secrets are available

## Main file

- `definitions/stg_employees.sqlx` creates the staging table from `raw_employees_ext`.

