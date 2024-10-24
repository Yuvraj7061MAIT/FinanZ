# Personal Finance Tracker API

The **Personal Finance Tracker API** is a backend application designed to help users track and manage their financial records. Built with **Node.js**, **Express**, and **MongoDB**, this API provides a simple and efficient way to create, read, update, and delete financial records.

## Table of Contents

- Features
- Tech Stack
- API Endpoints
- Installation
- Usage
- Contributing
- License
- Acknowledgements

## Features

- CRUD Operations: Create, read, update, and delete financial records.
- User-specific Data: Retrieve records based on user ID.
- Detailed Record Management: Track records with fields such as date, description, amount, category, and payment method.
- CORS Support: Easily connect from different front-end applications.

## Tech Stack
- Frontend: 
  - Type script
- Backend: 
  - Node.js
  - Express.js
- Database: 
  - MongoDB (Mongoose for ODM)
- Middleware: 
  - CORS for handling cross-origin requests
- Environment Variables: 
  - dotenv for managing environment configurations

## API Endpoints

### Financial Records

#### Get All Records by User ID

- **Endpoint**: `GET /financial-records/getAllByUserID/:userId`
- **Description**: Fetch all financial records for a specific user.
- **Parameters**: `userId`: The ID of the user.
- **Response**:
  - 200 OK: Returns an array of records.
  - 404 Not Found: No records found for the specified user.
  - 500 Internal Server Error: If there is an issue with the server.

#### Create a New Financial Record

- **Endpoint**: `POST /financial-records`
- **Description**: Create a new financial record.
- **Request Body**:
  ```
  {
    "userId": "string",
    "date": "YYYY-MM-DD",
    "description": "string",
    "amount": number,
    "category": "string",
    "paymentMethod": "string"
  }
  ```
- **Response**:
  - 200 OK: Returns the created record.
  - 500 Internal Server Error: If there is an issue with the server.

#### Update an Existing Financial Record

- **Endpoint**: `PUT /financial-records/:id`
- **Description**: Update an existing financial record by ID.
- **Parameters**: `id`: The ID of the record to update.
- **Request Body**:
  ```
  {
    "date": "YYYY-MM-DD",
    "description": "string",
    "amount": number,
    "category": "string",
    "paymentMethod": "string"
  }
  ```
- **Response**:
  - 200 OK: Returns the updated record.
  - 404 Not Found: Record not found with the specified ID.
  - 500 Internal Server Error: If there is an issue with the server.

#### Delete a Financial Record

- **Endpoint**: `DELETE /financial-records/:id`
- **Description**: Delete a financial record by ID.
- **Parameters**: `id`: The ID of the record to delete.
- **Response**:
  - 200 OK: Returns the deleted record.
  - 404 Not Found: Record not found with the specified ID.
  - 500 Internal Server Error: If there is an issue with the server.

## Installation

1. Install dependencies:
   ```
   npm install
   ```

2. Set up environment variables:
   Create a `.env` file in the root directory and add your MongoDB connection string:
   ```
   MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/databaseName
   ```

3. Start the server:
   ```
   npm run dev
   ```

4. The server will be running on `http://localhost:3001`.

## Usage

- Use tools like Postman or cURL to test the API endpoints.
- To get started, create financial records, retrieve them by user ID, and test update and delete functionalities.

## Contributing

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements

- Node.js for providing the runtime environment.
- Express.js for simplifying server-side development.
- MongoDB for providing the database.

---

This format can be directly copied into a text file. Let me know if you need any changes!
