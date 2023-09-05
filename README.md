# Steps to Start the DBT project
- Check ***PostgreSQL*** Version and Installation
    ```
        postgres -V
    ```
- Create a Virtual Enivornment for project using python
    ```
        virtualenv dbt_venv
    ```

- In virtual Env install the adapator for dbt and postgreSQL which will install ***dbt-core*** and ***dbt-postgres***

    ```
        pip install dbt-postgres
    ```


# Running the project 
-  Initialize the project 
    ``` 
        dbt init 
    ```

- Configure profiles for dbt

    ```
    dbt_for_medium:
    outputs:
    dev:
        type: postgres
        threads: 1
        host: localhost
        port: 5432
        user: dbt
        pass: dbtpass
        dbname: postgres
        schema: postgres
    prod:
        type: postgres
        threads: 1
        host: localhost
        port: 5432
        user: dbt
        pass: dbtpass
        dbname: postgres
        schema: postgres
    target: dev

    ```
