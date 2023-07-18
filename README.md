# dbt-sample-app
this is my first dbt application. I am trying out ways to explore this in order to create a quickstart.

# Python environment
Python 3.9.7
my anaconda environment name: test_ml

# Pip packages
pip install dbt-core
pip install dbt-postgres

# Package versions
dbt-core: 1.5.3
dbt-postgres: 1.5.3

# Initialise dbt application
dbt init

# Update .dbt/profiles.yml
## postgres configuration
ref: https://docs.getdbt.com/docs/core/connect-data-platform/postgres-setup
configuration used:
```
dev:
    type: postgres
    threads: 10
    host: 127.0.0.1
    port: 5432
    user: postgres
    pass: password
    dbname: dbt_db
    schema: dbt_schema
```

# PostgreSQL setup
create a database using the below script
```
CREATE DATABASE dbt_db
    WITH
    OWNER = postgres
    ENCODING = 'UTF8'
    CONNECTION LIMIT = -1
    IS_TEMPLATE = False;

GRANT ALL ON DATABASE dbt_db TO PUBLIC WITH GRANT OPTION;
```
# Check connection
navigate to the dbt application folder. Here, it is `dbt_app_1`. Now, run `dbt debug` to check if all checks are passed before starting to work on the repo
