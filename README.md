Documentation for Week3-API-Lab

# Setup Instructions 

1. Initialize the project:
   
      I created a new folder in VSCode named 'Week3-API-Lab' and opened a new
   terminal to initialize a node.js project with the command 'npm init -y' and
   to install required dependencies, I entered the command 'npm install express
   jsonwebtoken bcryptjs body-parser'.
   
3. Create server.js and Set up Express:
   
      In 'Week3-API-Lab' folder, I created a new file named 'server.js' and entered
   the code for server.js.
   
5. Testing the API using Postman:
   
      To test the API, I started the server with the command 'node server.js' and it
   should display something like 'Server running on port 3000'. After that, we will be
   able to test the endpoints in Postman:
   
   # Register a user
     1. Set the request type to POST an enter the URL: http://localhost:3000/api/register
     2. Go to Body -> select raw -> change the text to JSON and enter:
        
          {
              "username": "testuser",
              "password": "password123"
          }
        
        click SEND and you should get a response like:

          {
              "message": "User registered successfully"
          }
        
   # Login user
     1. Set the request type to POST an enter the URL: http://localhost:3000/api/login
     2. Go to Body -> select raw -> change the text to JSON and enter:
        
          {
              "username": "testuser",
              "password": "password123"
           }

        click SEND and you should get a response with a JWT token:

          {
              "token": "jwt_token_here"
          }
        
   # Access Protected Route
     1. Set the request type to GET an enter the URL: http://localhost:3000/api/protected
     2. Go to Headers and enter 'Authorization' for Key and 'Bearer your_jwt_token' for value
     3. click SEND and you will get a response like:
        
          {
              "message": "Hello, testuser! Welcome to the protected route."
          }

# Endpoints 
- 'POST /api/register' - to register a user
- 'POST /api/login' - to log in a user
- 'GET /api/protected' - to access the protected route
