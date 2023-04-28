# Country Information App

This application provides information about countries. It consists of a React frontend and an Express backend.

## Folder Structure

The application is seperated into two folder, client containing the react frontend, and server, containing the express backend.

## Dependencies

To run the application, several dependencies need to be installed. Here's a (hopefully) exhaustive list of packages I used in this project:

### Frontend:

- `axios`: for making HTTP requests.
- `@mui/material @emotion/react @emotion/styled`: for styling the app.
- `@testing-library/react @testing-library/jest-dom @testing-library/user-event`: for testing the app.

### Backend:

- `express`: for building the API.
- `axios`: for making HTTP requests.
- `concurrently nodemon --save-dev`: for running the backend and frontend concurrently during development.
- `jest supertest`: for testing the backend.
- `cors`: for enabling Cross-Origin Resource Sharing (CORS) in the backend.

## How to Run the App Locally

1. Navigate to the `server` directory in the terminal.
2. Start the server: `nodemon index.js`.
3. Open your web browser and navigate to `http://localhost:3001` to see the app running.

## Unit Tests

The Jest unit testing framework was used for unit testing both the frontend and the backend.

## How to Deploy the App

The application is already deployed at https://coding-challenge.herokuapp.com/. However, if you app isn't up for some reason, follow these instructions:

1. Navigate to the current directory in the terminal.
2. Log in to your Heroku profile: `heroku login`.
3. Initialize a Git repository: `git init`.
4. Add all files (recursively) in the current directory: `git add .`.
5. Commit the files: `git commit -m "<commit message>"`.
6. Enter the following command: `heroku git:remote -a coding-challenge`.
7. Push to the master branch: `git push heroku master`.
8. Navigate to the page: `heroku open`.

## Note on errors

In its current state, the program will return results when given partial information. For instance, giving it 'A' returns the information for 'Barbados'. This issue could be easily fixed in several ways, such as generating a whitelist of country names and checking that the query string is in the whitelist. However, I decided that this issue was minor and didn't require more attention, as it didn't obviously present a security issue and could be seen as a feature rather than a bug.















