# AnswerFisk | VANDYHACKS XI

[Project Documentation @ NOTION](https://chill-minute-c07.notion.site/Team-AnswerFisk-VANDYHACKS-XI-Sep-24-5d89d481a1a44395900d0f2023af1634)

[Presentation @ VandyHacks XI](https://www.canva.com/design/DAGSEfc1Fn4/qpJavwEB_dLSZUOodq-Uaw/edit?utm_content=DAGSEfc1Fn4&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

# Contributors:
- Manoj Bagale
- Zeal Okechukwu Achonu
- Osewuike Igue

## Prerequisites
- Basic understanding of Python programming
- Familiarity with web development and APIs

## Setup

1. **Create a Perplexity Account:**
   - Sign up for a Perplexity account and obtain your API key from the Perplexity dashboard.

2. **Environment Setup:**
   - Create a project directory:
     ```bash
     mkdir AnswerFisk
     cd AnswerFisk
     ```
   - Install Python from [python.org](https://www.python.org).
   - Install `virtualenv` to create an isolated environment:
     ```bash
     pip install virtualenv
     ```
   - Create and activate a virtual environment:
     ```bash
     virtualenv chatbot_env
     source chatbot_env/bin/activate
     ```

3. **Install Dependencies:**
   - Create a `requirements.txt` file with the following contents:
     ```txt
     Flask==2.0.3
     requests==2.25.1
     ```
   - Install the required dependencies:
     ```bash
     pip install -r requirements.txt
     ```

4. **Project Structure:**
   - Create the following folder structure:
     ```plaintext
     project_root/
     ├── app.py
     ├── static/
     │   ├── css/
     │   ├── js/
     │   └── assets/
     └── templates/
         ├── home.html
         └── chat.html
     ```

5. **Implementation:**
   - Create `app.py` with the basic Flask structure
   - Design `home.html` and `chat.html` for the chatbot interface within the `templates/` folder.
   - Set your API key as an environment variable:
     ```bash
     export API_KEY='your-api-key-here'
     ```

6. **Run the Application:**
   - Run the Flask app:
     ```bash
     python app.py
     ```
   - Open a web browser and go to `http://localhost:5000`.

## Features
- Web-based chat interface
- Integration with Meta's Llama model for AI-powered responses
  
