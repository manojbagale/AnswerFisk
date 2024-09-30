## AnswerFisk | Reimagining the digital experience at Fisk University
Documentation here: https://chill-minute-c07.notion.site/Team-AnswerFisk-VANDYHACKS-XI-Sep-24-5d89d481a1a44395900d0f2023af1634

## Prerequisites
Basic understanding of Python programming

Familiarity with web development and APIs

## Setup
Step 1: Perplexity Account
Sign up for an Perplexity account if you haven't already
Obtain your API key from the Perplexity dashboard

Step 2: Environment Setup
Create a new project directory
Install Python from https://www.python.org
Install virtualenv: pip install virtualenv
Create and activate a virtual environment:
virtualenv chatbot_env
source chatbot_env/bin/activate

Step 3: Install Dependencies
Install the required libraries

Step 4: Project Structure
Create the following project structure:
text
project_root/
│
├── app.py
├── static/
│   └── css
|   └── js
|   └── assets 
└── templates/
    └── home.html
    └── chat.html

Step 5: Implementation
Create app.py with the basic Flask application structure
Design the home.html template for the chatbot interface
Set your API key as an environment variable:
export API_KEY='your-api-key-here'

Run the Flask application:
python app.py

Open a web browser and navigate to http://localhost:5000

Features
Web-based chat interface
Integration with Meta's llama model
Real-time responses to responses regarding Fisk

