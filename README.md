# ✈️ Airport Management System

**Academic database project · SQL · Jupyter Notebook**

An educational project for exploring how relational databases represent airport operations. The repository bundles a SQL script and a notebook for experimentation.

## Contents

The source files are stored inside [`Project - Airport Management System.zip`](<Project - Airport Management System.zip>).

```text
Airport-Management-System/
├── README.md
└── Project - Airport Management System.zip
    ├── DBMS Project.sql
    └── Untitled6.ipynb
```

## Project objectives

- Model the relationships between airport-related records.
- Practice queries, constraints, and relational database design.
- Explore a database project in a Jupyter notebook.
- Apply database-management concepts to an airport domain.

> The existing project description discusses airlines, flights, passengers, bookings, and baggage. Consult the included `DBMS Project.sql` for the exact tables and operations actually implemented; those features have not been independently tested.

## Technology

| Component | Technology |
| --- | --- |
| Database work | SQL |
| Interactive exploration | Jupyter Notebook (`.ipynb`) |
| Notebook runtime | Python, if needed by notebook cells |

The database vendor and required Python packages are not specified at repository root.

## Getting started

### 1. Clone and extract

```bash
git clone https://github.com/syedasad09/Airport-Management-System.git
cd Airport-Management-System
```

Extract the ZIP file to a working directory.

### 2. Explore the SQL project

Open `DBMS Project.sql` in your database editor, identify the SQL dialect, and run it against a compatible **local test database**. Check statements before execution; different database engines use different syntax.

### 3. Open the notebook (optional)

Install Python 3 and Jupyter Notebook:

```bash
python -m pip install notebook
jupyter notebook
```

Open `Untitled6.ipynb` and review any imports, file paths, or connection settings before running cells.

## Known limitations

- This is an educational project, **not** software for a working airport.
- Database-engine compatibility and notebook requirements have not been verified.
- The source remains compressed rather than individually browsable on GitHub.
- Do not test with real passenger records or credentials.

## Suggested improvements

- Extract the SQL and notebook into visible `database/` and `notebooks/` directories.
- Add a verified database engine/version and sample dataset.
- Add an entity-relationship diagram based on the actual SQL schema.
- Provide setup screenshots and tested commands.

## Maintainer

[@syedasad09](https://github.com/syedasad09) · [Repository](https://github.com/syedasad09/Airport-Management-System)

## License

No repository-level `LICENSE` file is present. Please request permission before redistributing the code.
