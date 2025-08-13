# MERN Book App Backend

## Overview
This is the backend part of the MERN Book App, which allows users to create and manage books. The backend is built using Node.js, Express, and MongoDB with Mongoose for data modeling.

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd mern-book-app/backend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up MongoDB**
   Ensure you have MongoDB installed and running. You can use a local instance or a cloud service like MongoDB Atlas. Update the connection string in `src/app.js` as needed.

4. **Run the server**
   ```bash
   npm start
   ```

   The server will start on `http://localhost:5000` by default.

## API Endpoints

### Create a Book
- **Endpoint:** `POST /api/books`
- **Request Body:**
  ```json
  {
    "title": "Book Title",
    "author": "Author Name",
    "genre": "Genre"
  }
  ```
- **Response:**
  - **201 Created**: Returns the created book object.
  - **400 Bad Request**: Returns an error message if the request is invalid.

## Folder Structure
- `src/`: Contains the source code for the backend.
  - `controllers/`: Contains the logic for handling requests.
  - `models/`: Contains Mongoose models for data representation.
  - `routes/`: Contains route definitions for the API.
  - `app.js`: Entry point for the backend application.

## License
This project is licensed under the MIT License.