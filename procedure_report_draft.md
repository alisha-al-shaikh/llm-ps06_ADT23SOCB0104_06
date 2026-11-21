# Email Reply Assistant — Procedure Report

> **Important:** This is a report draft. Before submitting, fill in the student details and replace the testing/results notes with what you actually observed after running the application. Do not claim tests or screenshots that you have not completed.

## Header
**Project Title:** Email Reply Assistant  
**Problem Statement Number:** [Enter PS number]  
**Student Name:** [Enter name]  
**Roll Number:** [Enter roll number]  
**Class:** [Enter class/division]  
**GitHub Link:** [Paste public repository URL]

## Problem Statement
Writing professional email replies can take time, especially when the user needs to adjust the tone for different situations. The Email Reply Assistant accepts an email as input and uses a Large Language Model (LLM) to generate three labelled reply drafts: Formal, Friendly, and Short. It is intended to help users prepare clear and appropriate replies more efficiently.

## Tools and Model
- Programming language: Python
- User interface: Streamlit
- LLM: Google Gemini [confirm the exact model used]
- API integration: Google Gen AI Python SDK (`google-genai`)
- Environment variable support: `python-dotenv`
- Development environment: Visual Studio Code

## Procedure
1. Created a project folder named `Email-Reply-Assistant` and opened it in Visual Studio Code.
2. Created a Python virtual environment and installed the required packages using `pip install -r requirements.txt`.
3. Generated a Gemini API key using Google AI Studio and stored it in a local `.env` file. The key was not included in the source code or GitHub repository.
4. Designed a single prompt that instructs the LLM to produce exactly three replies with the headings FORMAL, FRIENDLY, and SHORT. The prompt also asks the model not to invent facts or commitments.
5. Wrote `app.py` to accept email text, build the prompt, call the Gemini API, and display the generated reply drafts.
6. Used Streamlit to create a text area and a Generate Replies button. Added input validation and error handling.
7. Ran the application locally using `streamlit run app.py`.
8. Tested the application with at least five sample emails and checked whether each output contained the three requested tones. [Replace this sentence with your actual test details.]
9. Captured screenshots of the working application and generated outputs for submission. [Add your actual screenshots.]

## Prompt Used
The application sends one prompt containing the following instructions, followed by the user's email:

“You are an email-writing assistant. Read the email and draft exactly three possible replies: FORMAL (professional and respectful), FRIENDLY (warm and conversational), and SHORT (concise and direct). Do not invent facts, promises, dates, attachments, or commitments. Use square-bracket placeholders where information is missing. Return the answer with the headings FORMAL, FRIENDLY, and SHORT.”

**Prompt improvement:** The prompt was strengthened by explicitly asking the model not to invent facts or commitments and to use placeholders when information is missing. This helps make the drafts safer to review and personalize.

## Results
[Complete this section after running the project.] Record the five sample email types tested and whether all three reply styles appeared for each. Insert one or two genuine screenshots showing the input and generated output. Do not report successful results unless you observed them.

## Challenges
[Write about the actual issues encountered.] Possible examples, only if they occurred: API-key configuration, package installation, internet connectivity, API quota limits, or inconsistent response formatting. Explain how each issue was resolved.

## Conclusion
The project demonstrates how a prompt-based LLM application can assist with a practical writing task. It combines Python, the Gemini API, and Streamlit to generate three email-reply styles from one input. A possible future improvement is to add controls for language, reply length, or a user-selected tone.
