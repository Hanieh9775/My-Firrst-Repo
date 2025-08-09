# app.py

from flask import Flask, render_template_string

app = Flask(__name__)

@app.route("/")
def home():
    return render_template_string("""
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Simple Web App</title>
    </head>
    <body>
        <h1>Hello, World!</h1>
        <p>This is a simple web application built with Flask.
    </body>
    </html>
    """)

if __name__ == "__main__":
    app.run(debug=True)

