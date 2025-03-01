
# ResumeATS Pro

**ResumeATS Pro** is a tool designed to help job seekers optimize their resumes for Applicant Tracking Systems (ATS) and improve their chances of landing their dream job. The application analyzes a resume (in PDF format) and provides insights based on a job description or other provided analysis options. The tool offers quick scanning, detailed analysis, and ATS optimization suggestions, powered by Google Generative AI.

## Features

- **Resume Analysis**: Analyze a resume (PDF) and get suggestions on improvement, key strengths, and ATS compatibility.
- **Job Description Parsing**: Optionally, provide a job description to tailor the resume analysis to the specific role.
- **ATS Optimization**: Get detailed recommendations to optimize the resume for ATS, including keyword suggestions and reformatting.
- **Quick Scan & Detailed Analysis**: Choose between a quick scan for an overview or a detailed analysis with in-depth feedback.
- **Interactive Chat**: Ask follow-up questions about the analysis and get detailed answers based on the resume and the analysis results.

## Tech Stack

### Backend (Node.js Implementation)
- **Express.js**: A web framework for handling HTTP requests and responses.
- **pdf-parse**: A library for extracting text from PDF files.
- **google-generative-ai**: A package to interact with Google’s Generative AI for generating content based on the resume and job description.
- **express-fileupload**: Middleware for handling file uploads.
- **body-parser**: Middleware to parse incoming request bodies.

### Frontend (Python Streamlit Implementation)
- **Streamlit**: A framework for building interactive web applications with Python.
- **google-generative-ai**: A Python package to interact with Google’s Generative AI for generating content.
- **PyPDF2**: A library for reading and extracting text from PDF files.
- **dotenv**: A package to load environment variables from `.env` files.

## Prerequisites

1. **Google API Key**: You need a valid Google API key to use Google Generative AI. Set it up in your environment variables (`GOOGLE_API_KEY`).
2. **Node.js (for the Express app)**: Ensure Node.js is installed to run the backend server.
3. **Python (for Streamlit app)**: Ensure Python 3.x is installed to run the Streamlit frontend.

## Installation

### Backend (Node.js Implementation)

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ResumeATS-Pro.git
   cd ResumeATS-Pro
   ```

2. Install the dependencies:
   ```bash
   npm install
   ```

3. Set up your environment variables by creating a `.env` file in the root directory and adding your Google API key:
   ```
   GOOGLE_API_KEY=your-google-api-key
   ```

4. Start the Express server:
   ```bash
   node server.js
   ```

5. The backend will be running at `http://localhost:3000`.

### Frontend (Streamlit Implementation)

1. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

2. Set up your environment variables by creating a `.env` file and adding your Google API key:
   ```
   GOOGLE_API_KEY=your-google-api-key
   ```

3. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

4. The frontend will be accessible at `http://localhost:8501`.


## Usage

### Backend API (Node.js)
- **Endpoint**: `/analyze` (POST)
- **Request Body**:
  - `resume`: The resume file (PDF) to be analyzed.
  - `jobDescription`: (Optional) The job description to tailor the analysis.
  - `analysisOption`: The type of analysis (`Quick Scan`, `Detailed Analysis`, `ATS Optimization`).

Example request:
```json
{
  "jobDescription": "Software Engineer position at XYZ",
  "analysisOption": "Detailed Analysis"
}
```

- **Response**:
  - JSON response containing the analysis results.

#### Testing the Node.js API:
1. Start the Node.js server by running:
   ```bash
   node index.js
   ```
2. Open the `index.html` file in a browser.
3. Upload the resume and enter an optional job description.
4. Choose the analysis option (`Quick Scan`, `Detailed Analysis`, or `ATS Optimization`).
5. Submit the form to see the analysis results.

### Frontend (Streamlit)
- **Run Streamlit App**:
  - First, install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
  - Then, run the Streamlit app:
    ```bash
    streamlit run app.py
    ```

- **Usage**:
  1. Upload your resume (PDF).
  2. Optionally, enter a job description.
  3. Choose the analysis type (`Quick Scan`, `Detailed Analysis`, or `ATS Optimization`).
  4. View the results of the analysis and ask follow-up questions about your resume.


## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Google Generative AI](https://cloud.google.com/generative-ai) for providing the AI services for resume analysis.
- [Streamlit](https://streamlit.io/) for creating a user-friendly web framework for building interactive applications.
- [pdf-parse](https://www.npmjs.com/package/pdf-parse) and [PyPDF2](https://pypi.org/project/PyPDF2/) for extracting text from PDF files.

---

Feel free to use this tool to improve your resume’s ATS compatibility and get tailored feedback for your job applications. If you have any questions, don't hesitate to reach out!
