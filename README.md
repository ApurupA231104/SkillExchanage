# SE-Project
Skill-Exchange

# SkillSync: A Skill and Knowledge Exchange Platform
Project Overview
SkillSync is a web application designed to connect users for skill, language, and peer tutoring exchanges. Users can create profiles listing skills they offer (e.g., JavaScript programming), skills they seek (e.g., Python), languages they speak (e.g., Spanish), or tutoring subjects they can teach or need help with. The platform matches users based on complementary needs, enabling collaborative learning. Built with a JavaScript frontend and a Node.js/MongoDB backend, SkillSync provides a user-friendly interface for profile management and match discovery.


# How to Run Locally
SkillSync is designed to run locally, as cloud deployment is not required per course guidelines. Follow these steps to set up and run the application on your machine.
Prerequisites

Node.js: Version 16 or higher (Download)
MongoDB: Local instance or MongoDB Atlas (Install)
Git: For cloning the repository (Download)
Browser: Chrome, Firefox, or Edge for the frontend

# Setup Steps

Clone the Repository:
git clone https://github.com/username/SkillSync.git
cd SkillSync

Install Dependencies:

Backend:cd src/server
npm install

Frontend (if using npm for static assets):cd src/client
npm install

Set Up MongoDB:
Start a local MongoDB instance:mongod

Alternatively, use MongoDB Atlas:
Create a free cluster at MongoDB Atlas.
Obtain the connection string (e.g., mongodb+srv://<user>:<password>@cluster0.mongodb.net/skillsync).

Configure Environment Variables:

Create a .env file in src/server:PORT=3000
MONGODB_URI=mongodb://localhost:27017/skillsync
JWT_SECRET=your_jwt_secret_here

Replace MONGODB_URI with your Atlas connection string if using Atlas.
Use a secure JWT_SECRET (e.g., a random 32-character string).

Run the Backend:
cd src/server
npm start

The server will run at http://localhost:3000.

Run the Frontend:
Use a static server for the client:cd src/client
npx http-server

Alternatively, open src/client/index.html directly in a browser (some features may require a server due to CORS).
Access the app at http://localhost:8080 (port may vary; check terminal output).

# Test the Application:
Navigate to http://localhost:8080.
Register a user (e.g., apple@gmail.com, password: test123).
Create a profile with skills (e.g., offer JavaScript, seek Python).
Explore the dashboard to view matches and edit your profile.
Test read-only mode by selecting another user’s profile (e.g., banana@gmail.com).

# Troubleshooting
MongoDB Connection Errors: Ensure MongoDB is running (mongod) or check your Atlas connection string.
CORS Issues: Use http-server instead of opening index.html directly.
JWT Errors: Verify JWT_SECRET matches in .env and is secure.
Port Conflicts: Change PORT in .env if 3000 is in use.

Demo Video
Watch our application running locally with a detailed code walkthrough:Demo VideoThis video demonstrates:

Setting up the project (cloning, installing, running).
Key features: user registration, profile creation, match browsing, profile editing.
Code explanation: frontend (script.js), backend (server.js), and configuration (.env).

Note: Replace the URL with the actual Google Drive or YouTube link after uploading the demo video.
Documentation
The following documents are included in the docs/ directory:

# Problem Statement: Outlines the need for a skill exchange platform and project goals.
Software Requirements Specification (SRS): Details functional and non-functional requirements, including user authentication and profile matching.
Software Design Document (SDD): Describes the MVC architecture, REST APIs, and MongoDB schema.

# Additional Notes for Evaluators
Code Quality: We adhered to ESLint standards for JavaScript and modularized code using the MVC pattern. Comments in script.js and server.js explain key logic.
Testing: Unit tests for backend APIs are in src/server/tests/. Frontend testing was manual due to time constraints.
Challenges Overcome:
Ensured secure profile editing with JWT authentication and client-side permission checks.
Optimized matching algorithm for case-insensitive skill/language comparisons.

Future Enhancements:
Implement real-time chat for user communication.
Add mobile app support with React Native.
Enhance matching with machine learning for better recommendations.

Why SkillSync Stands Out: Our platform empowers collaborative learning by connecting diverse users, with a scalable backend and intuitive UI.

Presntation and Demo videos : https://www.youtube.com/watch?v=X2aDUjqc2qA&list=PLNqgcZy6N9XtkyPqnOZItozDwCLgldpGP

# Thank you for evaluating SkillSync! #

