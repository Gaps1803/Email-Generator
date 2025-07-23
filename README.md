# 📧 AI-Powered Email Reply Generator

An intelligent full-stack application for generating professional email replies with the power of the Google Gemini API for the backend and a dynamic React.js interface for the frontend. This tool streamlines your communication by offering customizable tones and an innovative Optical Character Recognition (OCR) feature to extract text directly from images.

# 🌟 Features

Intelligent Email Reply Generation: Craft professional and contextually relevant email replies using the power of the Google Gemini API.

Customizable Tone: Choose from a variety of tones (e.g., Formal, Friendly, Concise, Appreciative) to match your communication style.

Optical Character Recognition (OCR): Effortlessly extract text from email screenshots or image files directly within the application, thanks to Tesseract.js.

User-Friendly Interface: A clean and intuitive React-based frontend for a seamless experience.

Clipboard Integration: Easily copy the generated email reply to your clipboard with a single click.

Cross-Origin Support: The Spring Boot backend is configured to allow requests from the React frontend application.

# 🚀 Technologies Used

This project leverages a modern tech stack for both its backend and frontend components.

Backend (Spring Boot)
Java 17: The core programming language.

Spring Boot 3.5.3: Framework for building robust, stand-alone, production-grade Spring applications.

Spring Web (spring-boot-starter-web): Provides core Spring MVC capabilities for building RESTful APIs.

Spring WebFlux (spring-boot-starter-webflux): Used for reactive, non-blocking HTTP requests with WebClient to interact with the Gemini API.

Lombok: Reduces boilerplate code (e.g., @Data, @AllArgsConstructor).

Jackson: For efficient JSON processing, specifically for parsing responses from the Gemini API.

Google Gemini API: The powerful large language model that performs the actual email reply generation.

Frontend (React)
React.js: A JavaScript library for building interactive user interfaces.

Vite: A fast build tool that enhances the frontend development experience.

Tesseract.js: A JavaScript library integrated for performing Optical Character Recognition (OCR) directly in the browser.

CSS: For comprehensive styling and responsive design of the user interface.

# ⚙️ Prerequisites

Before you begin, ensure you have the following software installed on your system:

Java Development Kit (JDK) 17 or higher

Apache Maven: For building and managing the backend dependencies.

Node.js (LTS version recommended)

npm (Node Package Manager, typically comes with Node.js) or Yarn

Google Gemini API Key
You will need a Google Gemini API key to allow the backend service to communicate with the Gemini model.

Visit the Google AI Studio to generate a new API key or retrieve an existing one.

Keep this key secure. It will be configured in your Spring Boot application's properties.

# 🛠️ Getting Started

Follow these steps to set up and run the Email Reply Generator on your local machine.

1. Clone the Repository
First, clone the project repository to your local machine:

Bash

git clone <your-repository-url>
cd email-generator # Navigate into the project directory
2. Backend Setup (Spring Boot)
Navigate to the email-generator directory, which contains the Spring Boot project.

Configuration
Create an application.properties file inside src/main/resources/ (if it doesn't already exist) and add the following lines, replacing YOUR_GEMINI_API_KEY with your actual key:

Properties

gemini.api.url=https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent?key=
gemini.api.key=YOUR_GEMINI_API_KEY
Build and Run the Backend
Use Maven to build and run the Spring Boot application:

Bash

# Clean and build the project, downloading dependencies
mvn clean install

# Run the Spring Boot application
mvn spring-boot:run
The backend service will start and be accessible at http://localhost:8080.

3. Frontend Setup (React)
Open a new terminal window and navigate to the same email-generator root directory. The React application is integrated within this structure.

Install Dependencies
Install the necessary Node.js packages for the React frontend:

Bash

npm install
# or
yarn install
Run the Frontend Application
Start the React development server:

Bash

npm run dev
# or
yarn dev
The frontend application will typically open in your default web browser at http://localhost:5173 (or another available port).

# 🚀 Usage

Once both the backend and frontend services are running:

Open your web browser and go to the frontend application URL (e.g., http://localhost:5173).

Input Original Email: In the "Original Email" text area, you can either:

Type or paste the email content you want to reply to.

Paste an image (e.g., a screenshot of an email) directly into the text area. The built-in OCR will process it and populate the text.

(Future enhancement: An explicit file upload button for images could be added for clarity, though pasting already works.)

Select Tone (Optional): Choose a desired tone from the dropdown menu (e.g., "Formal", "Friendly", "Professional") to influence the generated reply's style.

Generate Reply: Click the "Generate Reply" button. The application will send the email content and chosen tone to the backend for processing.

View and Copy Reply: The AI-generated email reply will appear in the "Generated Reply" box. Click the "Copy" button to instantly copy the reply to your clipboard for easy use.

# 📚 Project Structure

The project follows a standard Spring Boot and React application structure:

<img width="1016" height="574" alt="image" src="https://github.com/user-attachments/assets/4c0ff930-e947-4a65-8439-af01b5b46dfe" />


# 🤝 Contributing

We welcome contributions to enhance this Email Reply Generator! If you have ideas for improvements, new features, or bug fixes, please follow these steps:

Fork the repository on GitHub.

Clone your forked repository to your local machine.

Create a new branch for your feature or bug fix:

Bash

git checkout -b feature/your-feature-name
# or
git checkout -b bugfix/fix-issue-description
Make your desired changes to the codebase.

Commit your changes with a clear and descriptive message:

Bash

git commit -m "feat: Add new feature for X"
# or
git commit -m "fix: Resolve Y issue"
Push your changes to your forked repository:

Bash

git push origin feature/your-feature-name
Open a Pull Request to the main branch of the original repository. Provide a detailed description of your changes.

# 📄 License

This project is open-sourced under the MIT License (if you have this file in your project).
