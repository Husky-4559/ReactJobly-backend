## ReactJobly Backend
ReactJobly Backend is the server-side application for the ReactJobly project, a job board platform where users can search for companies and jobs, apply for positions, and manage their profiles. This backend provides a RESTful API that supports user authentication, job and company data retrieval, and application management.


### Table of Contents: 

	•	Features
	•	Installation
	•	Usage
	•	API Endpoints
	•	Technologies Used
	•	Contributing
	•	License
	•	Acknowledgments

### Features:
	•	User Authentication and Authorization: Secure login and registration using JWT tokens.
	•	CRUD Operations: Full create, read, update, and delete functionality for users, jobs, and companies.
	•	Role-Based Access Control: Admin and regular user permissions.
	•	Data Validation: Ensures data integrity and proper request handling.
	•	Error Handling: Consistent error responses for client and server errors.
	•	Secure Password Storage: Passwords are hashed using bcrypt.

### Installation:
Follow these steps to set up the project locally:
  1. Clone the repository
  git clone https://github.com/Husky-4559/ReactJobly-backend.git

  2. Navigate to the project directory
  cd ReactJobly-backend

  3. Install dependencies
  npm install

  4. Set up environment variables
  Create a .env file in the root directory with the following content:
    SECRET_KEY=your_secret_key
    PORT=3001
    DATABASE_URL=postgresql:///jobly
  •	Replace your_secret_key with a secure string.
	•	Ensure the DATABASE_URL matches your PostgreSQL configuration.

  5. Initialize the databse
    createdb jobly
    npm run db:migrate
    npm run db:seed

  6. Start the server
     npm start
  The server should now be running at http://localhost:3001.

### Usage
  	•	API Testing: Use tools like Postman or Insomnia to interact with the API endpoints.
	  •	Frontend Integration: Connect this backend to the ReactJobly frontend to see the full application in action.

### API Endpoints

  ### Authentication: 
	•	POST /auth/register - Register a new user.
	•	POST /auth/token - Authenticate a user and receive a JWT token.

 ### Users: 
	•	GET /users - Get a list of all users (admin only).
	•	GET /users/:username - Get details of a specific user.
	•	PATCH /users/:username - Update a user’s information.
	•	DELETE /users/:username - Delete a user.

  ### Companies:
  •	GET /companies - Get a list of all companies.
	•	GET /companies/:handle - Get details of a specific company.
	•	POST /companies - Create a new company (admin only).
	•	PATCH /companies/:handle - Update a company’s information (admin only).
	•	DELETE /companies/:handle - Delete a company (admin only).

  ### Jobs:
	•	GET /jobs - Get a list of all jobs.
	•	GET /jobs/:id - Get details of a specific job.
	•	POST /jobs - Create a new job (admin only).
	•	PATCH /jobs/:id - Update a job’s information (admin only).
	•	DELETE /jobs/:id - Delete a job (admin only).

 ### Applications:
	•	POST /users/:username/jobs/:id - Apply a user to a job.

 ### Technologies Used
	•	Node.js: JavaScript runtime environment.
	•	Express.js: Web framework for Node.js.
	•	PostgreSQL: Relational database management system.
	•	JWT (JSON Web Tokens): For secure user authentication.
	•	bcrypt: Library for hashing passwords.
	•	dotenv: Loads environment variables from a .env file.
	•	Express Validator: For validating and sanitizing user input.

### Contributing
Contributions are welcome! Please follow these steps:

	1.	Fork the repository.
	2.	Create a new branch: git checkout -b feature/YourFeature.
	3.	Commit your changes: git commit -m 'Add your feature'.
	4.	Push to the branch: git push origin feature/YourFeature.
	5.	Open a pull request.

### License
This project is licensed under the MIT License. 


### Acknowledgments
	•	Springboard: For project inspiration and guidance.
	•	Express.js: For the robust web framework.
	•	PostgreSQL: For the reliable database system.



























