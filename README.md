# Comments SPA Application

This project is a Single Page Application (SPA) that saves comments to a MySQL database.

## Features

- Users can leave comments by filling out a credential form with their email and username, which are saved locally in LocalStorage.
- To post a comment, users fill out a comment form that includes an alphanumeric CAPTCHA test. A JWT-encrypted CAPTCHA is sent to the user via cookies.
- Users can use four allowed HTML tags in their comments: `<i>`, `<a>`, `<strong>`, and `<code>`.
- Users can attach one image (JPEG, GIF, or PNG) that will be cropped to 320x240px and one text file (\*.txt) no larger than 100KB.
- Comments can be previewed before posting.
- Comments are validated to prevent broken HTML on the server side and are sent back to the client via WebSocket.
- Comments can be sorted by author, date, and email in both ascending and descending order.
- Only 25 comments are fetched per request.

## Technologies

- **Backend:** Express.js
- **Frontend:** React

## Docker Setup

To run the application in an isolated environment using Docker, follow these steps:

1. Download the project repository.
2. Navigate to the project directory in the command line.
3. Ensure Docker Engine is running.
4. Execute the command: `docker-compose up --build`

The backend and frontend will be available on ports 3000 and 5000, respectively.

- **Frontend URL:** [http://localhost:5000/comments-frontend/](http://localhost:5000/comments-frontend/)
- **Backend URL:** [http://localhost:3000](http://localhost:3000)

## Database

In the server folder, you'll find `schema.sql` for the database schema. Use MySQL Workbench or a similar program to apply the schema.

## Deployment

The app is hosted on GitHub and Heroku:

- **Frontend:** [https://sgrischenko8.github.io/comments-frontend/](https://sgrischenko8.github.io/comments-frontend/)
- **Backend:** [https://stark-dawn-12728-fe14e70c36ad.herokuapp.com/](https://stark-dawn-12728-fe14e70c36ad.herokuapp.com/)

Files live for one session on Heroku. In development mode, files are saved permanently in the server's "uploads" directory.

## Repositories

You can find the separate client and server parts at the following addresses:

- **Frontend:** [https://github.com/sgrischenko8/comments-frontend](https://github.com/sgrischenko8/comments-frontend)
- **Backend:** [https://github.com/sgrischenko8/comments-backend](https://github.com/sgrischenko8/comments-backend)

## Running Locally

To run the app locally:

1. Download the project.
2. Navigate to the project directory.
3. Install dependencies with `npm install`.
4. Start the application with `npm run dev`.

- **Backend:** Available at [http://localhost:3000](http://localhost:3000)
- **Frontend:** Available at [http://localhost:5000/comments-frontend/](http://localhost:5000/comments-frontend/)
