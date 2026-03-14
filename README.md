# **Serverless Notes API**

# 

# **Overview**

# **A serverless REST API built with \*\*AWS Lambda\*\*, \*\*Amazon API Gateway\*\*, \*\*Amazon DynamoDB\*\*, and \*\*AWS SAM\*\*.**  

# **The application supports full \*\*CRUD operations\*\* for managing notes and demonstrates how to build and deploy a serverless backend using Infrastructure as Code.**

# 

# **---**

# 

# **Features**

# 

# **- Create notes using a REST API**

# **- Retrieve notes by ID**

# **- Update note content**

# **- Delete notes**

# **- Fully serverless backend architecture**

# 

# **---**

# 

# **Architecture**

# 

# **Client → API Gateway → Lambda → DynamoDB**

# 

# **---**

# 

# **AWS Services Used**

# 

# **- AWS Lambda**

# **- Amazon API Gateway**

# **- Amazon DynamoDB**

# **- AWS IAM**

# **- AWS SAM**

# **- Amazon CloudWatch**

# 

# **---**

# 

# **Architecture Explanation**

# 

# **The client sends an HTTP request to \*\*Amazon API Gateway\*\*, which routes the request to the appropriate \*\*AWS Lambda\*\* function based on the HTTP method and endpoint.**

# 

# **Each Lambda function handles a specific operation such as creating, retrieving, updating, or deleting a note. The functions interact with the \*\*DynamoDB Notes table\*\* to store and retrieve data, while \*\*CloudWatch Logs\*\* captures execution logs for monitoring and troubleshooting.**

# 

# **---**

# 

# **Request Flow**

# 

# **1. The client sends a request to an API endpoint**  

# **2. API Gateway routes the request to the correct Lambda function**  

# **3. The Lambda function processes the request**  

# **4. DynamoDB stores or retrieves the note data**  

# **5. The API returns a JSON response to the client**  

# 

# **---**

# 

# **API Endpoints**

# 

# **Base URL:**

# 

# 

# **https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE**

# 

# 

# **Example:**

# 

# 

# **https://abc123.execute-api.us-east-1.amazonaws.com/Prod**

# 

# 

# **| Method | Endpoint | Description | Example cURL |**

# **|------|------|------|------|**

# **| \*\*POST\*\* | `/notes` | Create a new note | `curl -X POST "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes" -H "Content-Type: application/json" -d "{\\"content\\":\\"My first cloud note\\"}"` |**

# **| \*\*GET\*\* | `/notes/{id}` | Retrieve a note by ID | `curl "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID"` |**

# **| \*\*PUT\*\* | `/notes/{id}` | Update an existing note | `curl -X PUT "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID" -H "Content-Type: application/json" -d "{\\"content\\":\\"Updated note content\\"}"` |**

# **| \*\*DELETE\*\* | `/notes/{id}` | Delete a note | `curl -X DELETE "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID"` |**

# 

# **---**

# 

# **## Deployment**

# 

# **Build the application:**

# 

# 

# **sam build**

# 

# 

# **Deploy the infrastructure:**

# 

# 

# **sam deploy**

# 

# 

# **---**

# 

# **Monitoring**

# 

# **\*\*AWS CloudWatch Logs\*\* were used to monitor Lambda execution and troubleshoot API behavior during development and testing.**

# 

# **---**

# 

# **What I Learned**

# 

# **- How to build a serverless REST API using AWS services**  

# **- How Lambda integrates with API Gateway to process HTTP requests**  

# **- How DynamoDB stores and retrieves NoSQL data**  

# **- How to deploy infrastructure using \*\*AWS SAM (Infrastructure as Code)\*\***  

# **- How to debug and monitor serverless applications using CloudWatch**  

# 

# **---**

# 

# **Architecture Diagram**

# 

# **AWS\_serverless\_API\_architecture.jpg**

