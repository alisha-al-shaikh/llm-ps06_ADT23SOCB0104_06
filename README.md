# Email Reply Assistant

A small LLM-powered application that turns a pasted email into three possible replies: **Formal**, **Friendly**, and **Short**.

## Features
- Streamlit text area for the incoming email.
- One prompt sent to the Gemini API requesting three labelled drafts.
- Separate display sections for each reply.
- Basic input validation and API error handling.
- API key loaded from a local `.env` file rather than hard-coded.

## Technology
- Python
- Streamlit
- Google Gen AI Python SDK (`google-genai`)
- Gemini model: `gemini-2.5-flash`
- `python-dotenv`

## Setup (Windows / VS Code)

1. Install Python 3.10 or newer.
2. Open this folder in VS Code and create a virtual environment:

   ```powershell
   py -m venv venv
   venv\Scripts\activate
   ```

3. Install dependencies:

   ```powershell
   pip install -r requirements.txt
   ```

4. Copy `.env.example` to `.env`.
5. Add your own Gemini API key to `.env`:

   ```text
   GEMINI_API_KEY=your_actual_key
   ```

6. Start the application:

   ```powershell
   streamlit run app.py
   ```

## Testing
Test with at least five different non-sensitive sample emails (for example: meeting confirmation, deadline extension request, interview invitation, customer complaint, and thank-you email). Check that all three tones are present and that the drafts do not invent details. Capture screenshots of your actual running application and outputs in `screenshots/`.

## Security
- Never commit `.env` or share your API key.
- Do not use real confidential emails for testing.
- Review and personalize generated drafts before sending.

## Limitations
- The model may occasionally misunderstand context or produce imperfect wording.
- The application requires internet access and a working Gemini API key.
- Always review the generated draft before using it.
