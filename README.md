AI-Based-Online-E-Learning-Platform-with-Smart-Board-LLM-Tools

ASPIRO is a multi-module, AI-powered platform that makes learning more interactive, accessible, and personalized. It brings together intelligent learning assistance, educational resource recommendations, interactive 3D models, an online code playground, an AI-powered whiteboard, automated answer evaluation, and additional AI utilities in one project ecosystem.

The project combines modern web development technologies, AI APIs, data visualization, and Python-based services to explore how AI can improve digital education and give students more engaging learning experiences.

📌 Project Overview

Traditional learning platforms often provide the same resources to every student, offer limited interactivity, and require learners to switch between different applications for coding, studying, and obtaining feedback.

ASPIRO addresses these challenges by bringing several educational and AI-assisted tools under a common application interface. Students can explore learning resources, obtain personalized study recommendations, experiment with code, interact with AI-based tools, and access educational and wellness-related visualizations.

The project uses a modular architecture, with separate frontend applications and backend services responsible for different capabilities.

🎯 Objectives

- Provide personalized educational recommendations using generative AI.
- Improve learning through interactive 3D educational models.
- Offer a browser-based programming environment for practicing multiple languages.
- Explore AI-assisted calculations and visual problem-solving through a digital whiteboard.
- Automate answer evaluation and generate structured feedback.
- Convert video speech into text for further analysis and evaluation.
- Provide a chatbot interface with AI-generated text and audio responses.
- Present health-related metrics and learning analytics through visual dashboards.
- Build a modular foundation that can be extended with additional AI-powered features.

✨ Key Features

1. AI-Powered Learning Recommendations

The Student Learning Recommendation System uses Google's Gemini API to generate educational recommendations based on user preferences.

Capabilities include:
- Selection of educational level, such as high school, undergraduate, graduate, or professional development.
- Subject selection across areas such as computer science, mathematics, physics, biology, engineering, and business.
- Learning-style preferences, including visual, auditory, reading/writing, and kinesthetic learning.
- Difficulty-level selection and personalized learning goals.
- Weekly study-time preferences.
- Preferred learning resources, including courses, books, videos, tutorials, and projects.
- Learning history and recommendation data management.
- An analytics dashboard for examining learning activity and recommendation effectiveness.

2. Interactive 3D Learning Resources

The ASPIRO frontend includes a dedicated learning-resource section with interactive 3D educational models.

Available model categories include:
- Plant anatomy.
- Human heart anatomy.
- Digestive system.
- Microscope.

The models use 3D assets that can be viewed and manipulated in the browser, supporting a more visual approach to learning.

3. Online Code Playground

The Code Playground provides a browser-based environment for writing and executing code.

Features include:
- An interactive Monaco code editor.
- Language selection.
- Sample code snippets.
- A dedicated code output panel.
- Execution status and error feedback.
- API-based code execution through the Piston API.

Languages configured in the project:
- JavaScript
- TypeScript
- Python
- Java
- C#
- PHP

This module is useful for programming practice, experimenting with code, and learning programming concepts without requiring a separate local editor for every exercise.

4. AI Board and Visual Problem Solving

The AI Board module combines a React-based interface with a Python FastAPI backend.

The backend includes an image-processing endpoint that accepts image data, decodes it, and passes the resulting image to a calculation-analysis utility. The module is designed to support image-based mathematical problem processing and structured responses.

**Technologies and components include:**
- React and TypeScript.
- Vite.
- Tailwind CSS and Mantine UI.
- FastAPI.
- Python image processing with Pillow.
- Google Generative AI integration.
- Axios for HTTP communication.

5. Automated Answer Evaluation

The answer-evaluation backend provides an AI-assisted mechanism for assessing written responses.

Users can submit a question and an answer for evaluation. The service sends the content to Google's Gemini model and requests structured feedback based on four criteria:

- Relevance: How closely the answer addresses the question.
- Accuracy: Factual correctness and understanding of concepts.
- Structure: Organization, clarity, and logical flow.
- Language: Grammar, vocabulary, and writing quality.

The service requests criterion-wise scores, justifications, an overall score, and suggestions for improvement.

It also includes PDF report generation so that an evaluation can be presented as a downloadable document.

6. Video-to-Text Processing

The Python backend includes a video-upload workflow for extracting spoken content from video files.

Processing workflow:

1. Accept an uploaded video in a supported format.
2. Validate the file extension.
3. Save the video temporarily.
4. Extract audio using FFmpeg.
5. Process the audio using the SpeechRecognition library.
6. Convert recognized speech into text.
7. Return the extracted transcript to the frontend or calling application.
8. Remove temporary media files after successful processing.

Supported video extensions in the implementation include MP4, AVI, MOV, and MKV.

This capability can support lecture transcription, spoken-answer evaluation, and other educational workflows that use audio or video input.

7. AI Chatbot and Voice Output

The project also includes a Streamlit-based AI utility that accepts text input and generates responses using Google's Gemini API.

An optional voice feature converts the generated response into audio using Google Text-to-Speech (gTTS).

Features include:
- Text-based interaction.
- AI-generated responses.
- Text-to-speech conversion.
- In-browser audio playback.
- Audio download functionality.

This module demonstrates how generative AI and speech synthesis can be combined to provide an alternative way to consume information.

8. Health Monitoring and Analytics Dashboards

The ASPIRO frontend includes a health-monitoring dashboard with chart-based visualizations.

The interface displays sample metrics and charts related to vital signs, activity, nutrition, stress, and daily statistics. These visualizations demonstrate how health-related information can be organized into a dashboard.

The student recommendation module separately includes an analytics dashboard for sample user-engagement trends, subject popularity, retention patterns, and recommendation feedback.

Important: The included health dashboard uses predefined sample values. It should not be represented as a validated medical monitoring system or as a source of real-time clinical measurements.

🛠️ Technology Stack

Frontend

| Technology | Purpose |
|---|---|
| React 18 | Component-based user interface development |
| JavaScript (ES6+) | Frontend logic and interactions |
| TypeScript | Type-safe development in the AI Board frontend |
| Vite | Development server and build tooling |
| React Router | Client-side navigation |
| Tailwind CSS | Utility-first styling |
| Framer Motion | UI animations and transitions |
| Chakra UI | Code Playground interface components |
| Mantine UI | AI Board interface components |
| Monaco Editor | Browser-based code editing |
| Recharts | Dashboard visualizations |
| Lucide React / Heroicons | Interface icons |
| Axios | HTTP requests to external APIs and services |

Backend

| Technology | Purpose |
|---|---|
| Python | AI utilities, data processing, and backend logic |
| FastAPI | API endpoints for the AI Board module |
| Flask | Video processing and answer-evaluation endpoints |
| Node.js | JavaScript server runtime |
| Express.js | ASPIRO backend API framework |
| MongoDB | Database integration through Mongoose |
| Mongoose | MongoDB object modeling |
| JWT | Token-based authentication |
| bcryptjs | Password hashing in the Node.js backend |
| CORS | Cross-origin request configuration |
| Uvicorn | ASGI server for FastAPI |

Artificial Intelligence and Processing

| Technology | Purpose |
|---|---|
| Google Gemini API | AI-generated recommendations, responses, and evaluation |
| Google Generative AI SDK | Python integration with Gemini |
| Piston API | Remote code execution |
| SpeechRecognition | Speech-to-text processing |
| FFmpeg | Audio extraction from video files |
| Pillow | Image decoding and processing |
| gTTS | Text-to-speech conversion |
| ReportLab | PDF evaluation report generation |

Data Handling and Visualization

- JSON files for student profiles, preferences, recommendations, and feedback.
- Pandas for tabular data processing.
- Plotly for interactive analytics charts.
- Recharts for frontend dashboard visualizations.
- Python logging for application diagnostics.

Technology lists reflect the supplied source code and dependency manifests. Not every listed technology is used by every module.

🏗️ System Architecture

The project follows a modular architecture in which the frontend interfaces communicate with separate backend services and external APIs.

```text
                         ASPIRO PLATFORM
                                |
              +-----------------+-----------------+
              |                 |                 |
        Main Web UI       Learning Tools     AI Utilities
              |                 |                 |
        React + Vite     +------+-------+    +----+------+
              |           |      |       |    |           |
        Express API    3D Models  AI    Code  Chatbot   Evaluation
              |                  Board  Editor    |          |
        MongoDB                  |      |     Gemini API  Flask API
                                 |      |
                              FastAPI  Piston API
                                 |
                         Image Analysis Utility

        Additional Services:
        - Student Recommendation System (Streamlit + Gemini)
        - Video-to-Text Processing (Flask + FFmpeg + SpeechRecognition)
        - Health and Learning Analytics Dashboards
```

The diagram represents the logical grouping of the supplied modules, not a claim that every component currently runs through a single integrated backend. Some modules use separate development servers and API endpoints.

📂 Project Structure

The supplied archives contain the following main application directories. If you combine them into one GitHub repository, organize the folders consistently and update the paths in the commands below to match your final structure.

```text
ASPIRO/
├── Aspiro/
│   ├── frontend/
│   │   ├── src/
│   │   │   ├── components/
│   │   │   ├── pages/
│   │   │   └── services/
│   │   ├── public/
│   │   └── package.json
│   └── server/
│       ├── config/
│       ├── middleware/
│       ├── models/
│       ├── routes/
│       └── server.js
│
├── ai-board/
│   ├── board/
│   │   └── src/
│   └── backend/
│       ├── apps/
│       ├── main.py
│       └── requirements.txt
│
├── codeplayground/
│   └── code/
│       ├── src/
│       │   └── components/
│       └── package.json
│
├── student-recommendation-system/
│   ├── app/
│   ├── api/
│   ├── data/
│   ├── analytics/
│   └── requirements.txt
│
├── backend/
│   ├── app.py
│   ├── models/
│   ├── templates/
│   ├── uploads/
│   └── reports/
│
└── mm/
    └── mm/
        └── onlineai.py
```

⚙️ Installation and Setup

 Prerequisites

Install the following tools before running the relevant modules:

- Node.js and npm.
- Python 3.9 or a compatible Python version for the selected dependencies.
- MongoDB for the ASPIRO authentication backend.
- FFmpeg for video-to-audio conversion.
- A Google Gemini API key for modules that use Gemini.
- Internet access for external API calls and remote code execution.

1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/ASPIRO.git
cd ASPIRO
```

Replace `YOUR_USERNAME` with your GitHub username and `ASPIRO` with your actual repository name if different.

2. Start the ASPIRO Frontend

```bash
cd Aspiro/frontend
npm install
npm run dev
```

Vite will display the local development URL in the terminal.

3. Start the ASPIRO Backend

Open another terminal:

```bash
cd Aspiro/server
npm install
node server.js
```

Configure the required environment variables before starting the server.

Example `.env` configuration:

```env
PORT=5006
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secure_random_secret
```

The server provides registration and login routes under `/api/auth`.

4. Start the AI Board Backend

```bash
cd ai-board/backend
python -m venv venv
```

Activate the environment on Windows:

```powershell
venv\Scripts\Activate.ps1
```

On macOS or Linux:

```bash
source venv/bin/activate
```

Install dependencies and start the API:

```bash
pip install -r requirements.txt
uvicorn main:app --reload --host 127.0.0.1 --port 8900
```

Configure any required Gemini credentials using environment variables.

5. Start the Code Playground

```bash
cd codeplayground/code
npm install
npm run dev
```

The Code Playground uses the Piston API for remote code execution. Execution therefore depends on network access and the availability of that external service.

6. Start the Student Recommendation System

```bash
cd student-recommendation-system
python -m venv venv
```

Activate the virtual environment using the command for your operating system, then run:

```bash
pip install -r requirements.txt
```

Create a `.env` file with the required Gemini credential:

```env
GOOGLE_API_KEY=your_gemini_api_key
```

Launch the main application:

```bash
streamlit run app/app.py
```

The analytics dashboard can be launched separately:

```bash
streamlit run analytics/dashboard.py
```

7. Start the Answer Evaluation and Video Processing Backend

```bash
cd backend
python -m venv venv
```

Activate the environment and install the dependencies required by the application. Ensure FFmpeg is installed and available on your system's PATH.

The application entry point is `app.py`:

```bash
python app.py
```

The exact Python dependencies should be documented in a dedicated `requirements.txt` for this module before distributing the repository.

8. Start the AI Chatbot

```bash
cd mm/mm
pip install streamlit google-generativeai gTTS
streamlit run onlineai.py
```

Configure the Gemini API credential securely before starting the chatbot.

 These commands start the modules individually. Port configuration, API URLs, environment variables, and cross-module integration may need adjustment to match your final deployment setup.

🔐 Security and Configuration

Security should be addressed before making the repository public.

- Never commit API keys, passwords, JWT secrets, database connection strings, or private configuration files.
- Store credentials in environment variables and load them using `python-dotenv` or Node.js `dotenv`.
- Add `.env`, `.env.local`, virtual environments, `node_modules`, generated reports, uploads, and temporary files to `.gitignore` where appropriate.
- Rotate any API keys that have already been exposed in source files or committed to Git history.
- Keep authentication secrets strong and use HTTPS in production.
- Validate uploaded files and limit their size.
- Apply appropriate authentication, authorization, rate limits, and error handling to production APIs.
- Do not rely on sample dashboard data for medical or academic decisions.

🚀 Potential Future Improvements

- Integrate all modules through a centralized API gateway.
- Replace local JSON-based persistence with a database where appropriate.
- Add role-based access for students, teachers, and administrators.
- Implement comprehensive automated tests and API documentation.
- Add persistent learning-progress tracking and recommendation feedback.
- Improve accessibility, responsive design, and keyboard navigation.
- Add production deployment configuration using Docker.
- Implement monitoring, structured logging, and secure file retention.
- Connect health dashboards to validated data sources if real monitoring is intended.

🎓 Learning Outcomes

This project provides practical experience with:

- Full-stack application development.
- REST API design and integration.
- React component architecture and client-side routing.
- Python-based backend development.
- Generative AI API integration and prompt design.
- Code editor integration and remote code execution.
- Speech recognition and text-to-speech workflows.
- Image processing and document generation.
- MongoDB integration and authentication fundamentals.
- Data persistence, analytics, and dashboard development.
- Environment configuration and multi-service application setup.

📄 Conclusion

ASPIRO demonstrates how multiple AI-assisted educational and productivity tools can be organized into a modular digital platform. By combining personalized learning recommendations, interactive 3D resources, programming tools, AI-powered assessment, speech processing, and analytics, the project explores several practical applications of artificial intelligence in education.

The codebase serves as a foundation for further integration, testing, accessibility improvements, and deployment as a more complete learning platform.

---

Project: ASPIRO — AI-Powered Learning, Education & Smart Assistance Platform  
Category: Full-Stack Development, Artificial Intelligence, EdTech  
Primary Technologies: React, TypeScript, JavaScript, Node.js, Express.js, Python, FastAPI, Flask, MongoDB, Streamlit, and Google Gemini API  
Status: Modular development project; individual services and integration should be verified before production deployment.
