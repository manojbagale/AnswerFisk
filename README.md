# AnswerFisk | Reimagining the Digital Experience at Fisk University

**Project Documentation**: [Link to Notion Documentation](https://chill-minute-c07.notion.site/Team-AnswerFisk-VANDYHACKS-XI-Sep-24-5d89d481a1a44395900d0f2023af1634)

## Prerequisites
- Basic understanding of **Python programming**
- Familiarity with **web development** and **APIs**

## Setup

### Step 1: Create a Perplexity Account
1. Sign up for a **Perplexity** account if you haven't already.
2. Obtain your API key from the Perplexity dashboard.

### Step 2: Environment Setup
1. Create a new project directory:
   ```bash
   mkdir AnswerFisk
   cd AnswerFisk
Install Python from the official Python website.

Install virtualenv to create an isolated environment:

bash
Copy code
pip install virtualenv
Create and activate a virtual environment:

bash
Copy code
virtualenv chatbot_env
source chatbot_env/bin/activate
Step 3: Install Dependencies
Install the required libraries (Flask, requests, etc.) by creating a requirements.txt file:

makefile
Copy code
Flask==2.0.3
requests==2.25.1
Install the dependencies:

bash
Copy code
pip install -r requirements.txt
Step 4: Project Structure
Create the following folder structure:

arduino
Copy code
project_root/
│
├── app.py
├── static/
│   ├── css/
│   ├── js/
│   └── assets/
└── templates/
    ├── home.html
    └── chat.html
Step 5: Implementation
Create the app.py file with a basic Flask structure for the chatbot.

Design the home.html template for the chatbot interface inside the templates/ folder.

Set your API key as an environment variable:

bash
Copy code
export API_KEY='your-api-key-here'
Run the Flask application:

bash
Copy code
python app.py
Open your web browser and navigate to http://localhost:5000.

Features
Web-based chat interface: A clean and interactive web interface for user interaction.
Integration with Meta's Llama model: Uses Perplexity API with the Llama model to deliver responses.
Real-time responses: Provides answers to questions specific to Fisk University.
