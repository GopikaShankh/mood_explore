# Mood Tracker Application

## Overview

This project is a full-stack application for tracking moods. It consists of a frontend built with React and a backend built with Node.js and Express. The application allows users to submit their moods, view a history of their moods, and receive suggestions based on their mood.

## Project Structureclient/
        client/
        package.json
        public/
            index.html
            manifest.json
            robots.txt
        README.md
        src/
            App.css
            App.js
            components/
                Dashboard.js
                History.js
                HomePage.css
                HomePage.js
                Login.css
                Login.js
                MoodForm.js
                MoodList.js
                navbar.js
            index.css
            index.js
    server/
        .env
        geminiApi.js
        index.js
        models/
            mood.js
        package.json
        README.md
        routes/
            moodRouter.js
## Backend

### Dependencies

- [`express`](/home/navgurukul/.cache/typescript/5.7/node_modules/@types/express/index.d.ts ): Web framework for Node.js
- [`mongoose`](server/node_modules/mongoose/types/aggregate.d.ts ): MongoDB object modeling tool
- [`dotenv`](server/node_modules/dotenv/lib/main.d.ts ): Loads environment variables from a [`server/.env`](server/.env ) file
- [`cors`](/home/navgurukul/.cache/typescript/5.7/node_modules/@types/cors/index.d.ts ): Middleware for enabling CORS
- `@google/generative-ai`: Google Generative AI library

### Environment Variables

- [`MONGO_URI`](/home/navgurukul/.cache/typescript/5.7/node_modules/@types/node/globals.d.ts ): MongoDB connection string
- [`PORT`](/home/navgurukul/.cache/typescript/5.7/node_modules/@types/node/globals.d.ts ): Port number for the server
- [`GEMINI_API_KEY`](/home/navgurukul/.cache/typescript/5.7/node_modules/@types/node/globals.d.ts ): API key for Google Generative AI

### Files

- [`server/index.js`](server/index.js ): Entry point for the backend server.
- [`server/models/mood.js`](server/models/mood.js ): Mongoose model for mood data.
- [`server/routes/moodRouter.js`](server/routes/moodRouter.js ): Express router for handling mood-related routes.
- [`server/geminiApi.js`](server/geminiApi.js ): Module for interacting with Google Generative AI.

### Routes

- `POST /`: Adds a new mood entry.
- `GET /`: Retrieves all mood entries.
- `DELETE /:id`: Deletes a mood entry by ID.

### Running the Backend

1. Install dependencies:
    ```sh
    npm install
    ```
2. Start the server:
    ```sh
    npm run dev
    ```

## Frontend

### Dependencies

- `react`: JavaScript library for building user interfaces
- `react-dom`: React package for working with the DOM
- `react-router-dom`: Declarative routing for React
- [`axios`](client/node_modules/axios/index.d.ts ): Promise-based HTTP client

### Files

- [`client/src/index.js`](client/src/index.js ): Entry point for the React application.
- [`client/src/App.js`](client/src/App.js ): Main application component with routing.
- [`client/src/components`](client/src/components ): Directory containing React components.

### Components

- [`Dashboard`](client/src/components/Dashboard.js ): Displays the latest mood and a form to submit new moods.
- [`History`](client/src/components/History.js ): Displays a list of all moods.
- [`HomePage`](client/src/components/HomePage.js ): Landing page with a description and login button.
- [`Login`](client/src/components/Login.js ): Form for user login.
- [`MoodForm`](client/src/components/MoodForm.js ): Form for submitting a new mood.
- [`MoodList`](client/src/components/MoodList.js ): List of moods with delete functionality.
- [`Navbar`](client/src/components/navbar.js ): Navigation bar.

### Running the Frontend

1. Install dependencies:
    ```sh
    npm install
    ```
2. Start the development server:
    ```sh
    npm start
    ```

## Usage

1. Navigate to the homepage.
2. Login or create an account.
3. Submit your mood using the form on the dashboard.
4. View your mood history and delete entries if needed.
