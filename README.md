# Miniblog

It's a project to put in practice all the key concepts of Flask along with other libraries as ninja2, WFTFlask to manage form and SQLAlchemy for DB.

## Execution time

Once we are ready to run the project, we'll to follow the next steps:

### Make sure you're in the right location

Make sure you're in right env and in case you need the command to active your env. Here you have it.

envname\Scripts\[activate|desactivate]

### Creating DB Tables

To create tables automatically first of all you need the right config in the SQLALCHEMY_DATABASE_URI property for psotgresql in my case the connection string is postgresql://<username>:<password>@localhost:5432/<dbname>

Then, staying inside the project folder you can run the next command:

python -m idlelib.idle

finally, we can run the command for creation...


    from run import app, db

    with app.app_context():

        db.create_all()

### Running the app

Once you had the env activated (commands below again).

        .\venv\Scripts\activate  # Windows
        source venv/bin/activate  # macOS/Linux

set the Flask App variable.

        set FLASK_APP=run.py  # Windows
        export FLASK_APP=run.py  # macOS/Linux

finally, we run the app with the next command:

        flask run