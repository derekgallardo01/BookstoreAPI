## Getting Started

1.  Create and activate virtual environment
    ```
    python3 -m venv venv
    source venv/bin/activate
    ```
2.  Install packages
    ```
    pip install -r requirements.txt
    ```
3.  Create .**env** file
    ```
    touch .env
    ```
4.  Set required environment variables in **.env** file
    ```
    FLASK_RUN_PORT='8080'
    FLASK_APP='app.py'
    FLASK_DEBUG='True'
    SECRET_KEY='some_secret_key'
    SQLALCHEMY_TRACK_MODIFICATIONS='False'
    <!-- Use one of the following: -->
    SQLALCHEMY_DATABASE_URI='sqlite:///db.sqlite' # sqlite
    SQLALCHEMY_DATABASE_URI='sqlite:///:memory:' # in-memory sqlite
    SQLALCHEMY_DATABASE_URI='postgresql://postgres:postgres@localhost:5432/bookstore' # postgresql
    ```
5.  Run tests
    ```
    pytest
    ```
6.  If using postgresql, run the database server, install **psql**, and create a database
    ```
    psql -c "CREATE DATABASE bookstore;"
    ```
7.  Run app db commands
    ```
    flask db drop
    flask db migrate
    flask db seed
    ```
8.  Start app
    ```
    flask run
    ```
