# AnswerFisk | Reimagining the Digital Experience at Fisk University

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
   - Create `app.py` with the following basic Flask structure:
     ```python
     from flask import Flask, render_template, request
     import requests

     app = Flask(__name__)
     api_key = "your-api-key-here"  # Replace with your actual API key

     def get_completion(prompt):
         url = "https://api.perplexity.ai/chat/completions"
         payload = {
             "model": "llama-3.1-sonar-small-128k-online",
             "messages": [
                 {"role": "system", "content": "Respond to greeting simply and precisely."},
                 {"role": "user", "content": prompt},
             ],
             "max_tokens": "84",
             "temperature": 0.2,
             "top_p": 0.9,
             "return_citations": True,
             "search_domain_filter": ["perplexity.ai"],
             "return_images": False,
             "return_related_questions": False,
             "search_recency_filter": "month",
             "top_k": 0,
             "stream": False,
             "presence_penalty": 0,
             "frequency_penalty": 1
         }
         headers = {
             "Authorization": f"Bearer {api_key}",
             "Content-Type": "application/json"
         }

         response = requests.post(url, json=payload, headers=headers)

         if response.status_code == 200:
             response_json = response.json()
             return response_json['choices'][0]['message']['content']
         else:
             return "Error: Unable to connect to the API."

     @app.route("/")
     def home():
         return render_template("home.html")

     @app.route("/get")
     def get_bot_response():
         userText = request.args.get('msg')
         response = get_completion(userText)
         return response

     if __name__ == "__main__":
         app.run()
     ```

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

## Some screenshots: 
![AnswerFisk](static/assets/Screenshot(144).png "AnswerFisk Logo")
![AnswerFisk](static/assets/Screenshot(146).png "AnswerFisk Logo")

