Intro to Flask and API basics

Setup Steps
Make a venv with the command: python3 -m venv venv
Activate the venv.
Linux & Mac: source venv/bin/activate
Windows: .\venv\Scripts\Activate
Install Flask with pip install flask
Install python-dotenv with pip install python-dotenv
Preserve our packages into a requirements file with: pip freeze > requirements.txt
Make a .env file in the root of the repo.
Make an app.py file in the root of the repo.
Copy this code into the app.py file:
from flask import Flask

app = Flask(__name__)

print(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"
Run the server with flask run in the terminal.

Move the app.py file into a src directory, make the directory if you have to!

Go to our .env file and add FLASK_APP=src/app.py to the file.

To enable hot reloading, enable debug mode. Add this to the .env file: FLASK_DEBUG=1
