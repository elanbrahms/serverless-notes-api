# **Serverless Notes API**

# 

# **Overview**

##### A serverless REST API built with AWS Lambda, API Gateway, DynamoDB, and AWS SAM. The application supports full CRUD operations for notes.

# 

# **Architecture**

##### Client → API Gateway → Lambda → DynamoDB

# 

# **AWS Services Used**

##### \- AWS Lambda

##### \- API Gateway

##### \- DynamoDB

##### \- IAM

##### \- AWS SAM

##### \- CloudWatch

# 

# **API Endpoints**

##### \- POST /notes

##### \- GET /notes/{id}

##### \- PUT /notes/{id}

##### \- DELETE /notes/{id}

# 

# **Architecture Explanation**



###### The client sends an HTTP request to Amazon API Gateway, which routes the request to the appropriate AWS Lambda function based on the HTTP method and endpoint. Each Lambda function handles a specific operation such as creating, retrieving, updating, or deleting a note. The functions interact with the DynamoDB Notes table to store and retrieve data, while CloudWatch Logs captures execution logs for monitoring and troubleshooting.

###### 

##### **Request Flow**

###### 

1. The client sends a request to an API endpoint

   ---
2. API Gateway routes the request to the correct Lambda function

   ---
3. The Lambda function processes the request

   ---
4. DynamoDB stores or returns the note data

   ---
5. ###### The API returns a JSON response to the client







# API Endpoints

# 

# Base URL:  

# `https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE`

# 

# Example:  

# `https://abc123.execute-api.us-east-1.amazonaws.com/Prod`

# 

# | Method | Endpoint | Description | Example cURL |

# |------|------|------|------|



# | \*\*POST\*\* | `/notes` | Create a new note | `curl -X POST "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes" -H "Content-Type: application/json" -d "{\\"content\\":\\"My first cloud note\\"}"` |



# | \*\*GET\*\* | `/notes/{id}` | Retrieve a note by ID | `curl "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID"` |



# | \*\*PUT\*\* | `/notes/{id}` | Update an existing note | `curl -X PUT "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID" -H "Content-Type: application/json" -d "{\\"content\\":\\"Updated note content\\"}"` |



# | \*\*DELETE\*\* | `/notes/{id}` | Delete a note | `curl -X DELETE "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID"` |





# Deployment

##### sam build

##### sam deploy





# Monitoring

##### AWS CloudWatch logs were used to troubleshoot Lambda execution and validate API behavior during testing.

# 

# What I Learned

##### \- How to build a serverless API

##### \- How Lambda integrates with API Gateway

##### \- How DynamoDB stores NoSQL data

##### \- How to deploy infrastructure using AWS SAM



# Architecture Diagram

# AWS\_serverless\_API\_architecture.jpg

