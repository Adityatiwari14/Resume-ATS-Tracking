# ATS Resume Expert

## Overview
This project is an ATS (Applicant Tracking System) Resume Evaluation tool built with Streamlit. It analyzes a resume (PDF) against a provided job description using Google Gemini Pro Vision to assess the match percentage and highlight missing keywords.

## Project Structure
- `.env` - Contains API keys and environment variables.
- `app.py` - The main Streamlit web application for resume evaluation.
- `requirements.txt` - Dependencies required to run the project.

## Features
- Uploads and processes PDF resumes.
- Extracts the first page of the resume for analysis.
- Compares the resume with a job description using Google Gemini Pro Vision.
- Provides an ATS-style evaluation, including:
  - **Strengths and weaknesses** of the candidate.
  - **Percentage match** with the job description.
  - **Missing keywords** and **final suggestions**.

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up environment variables:
   - Create a `.env` file in the project root.
   - Add the Google API key:
     ```
     GOOGLE_API_KEY="your_google_api_key_here"
     ```

## Usage
1. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```
2. Enter the job description in the text area.
3. Upload a resume (PDF format).
4. Click the appropriate button:
   - **"Tell Me About the Resume"** - Provides a detailed evaluation of the resume.
   - **"Percentage Match"** - Gives a match percentage and missing keywords.

## Explanation of Files
### `.env`
- Stores the `GOOGLE_API_KEY` used for accessing the Google Gemini Pro API.
- **Ensure this file is not shared publicly to protect sensitive credentials.**

### `app.py`
- Loads environment variables using `dotenv`.
- Processes uploaded resumes, extracts content, and converts it into an image.
- Sends extracted data to Google Gemini Pro Vision for analysis.
- Returns feedback on resume alignment with the job description.

### `requirements.txt`
- Lists all required dependencies:
  - `streamlit`: Creates an interactive web app.
  - `google-generativeai`: Connects to Google Gemini Pro for analysis.
  - `python-dotenv`: Manages environment variables.
  - `pdf2image`: Converts PDFs into images for processing.

## Contributing
Contributions are welcome! Feel free to submit issues and pull requests to improve the project.

## License
This project is licensed under the MIT License. See `LICENSE` for details.
