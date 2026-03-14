# Serverless Notes API

## Overview

The **Serverless Notes API** is a REST API built on AWS that supports
full CRUD operations for notes.  
It uses **Amazon API Gateway** to expose HTTP endpoints, **AWS Lambda**
to run backend logic, and **Amazon DynamoDB** to store note data.

Infrastructure is deployed using **AWS SAM**, demonstrating how to build
and manage serverless applications with Infrastructure as Code.

\---

## Features

* Create notes
* Retrieve notes by ID
* Update note content
* Delete notes
* Fully serverless backend architecture

\---

## Architecture

Client → API Gateway → Lambda → DynamoDB

\---

## AWS Services Used

* AWS Lambda
* Amazon API Gateway
* Amazon DynamoDB
* AWS IAM
* AWS SAM
* Amazon CloudWatch

\---

## Architecture Explanation

The client sends an HTTP request to **Amazon API Gateway**, which routes
the request to the appropriate **AWS Lambda** function based on the HTTP
method and endpoint.

Each Lambda function handles a specific operation such as creating,
retrieving, updating, or deleting a note. The functions interact with
the **DynamoDB Notes table** to store and retrieve data.

Execution logs are automatically captured in **Amazon CloudWatch Logs**,
which helps with monitoring and debugging the application.

\---

## Request Flow

1. The client sends a request to an API endpoint\\
2. API Gateway routes the request to the appropriate Lambda function\\
3. The Lambda function processes the request\\
4. DynamoDB stores or retrieves the note data\\
5. The API returns a JSON response to the client

\---

# API Endpoints

### Base URL

&#x20;   https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE



Example:

&#x20;   https://abc123.execute-api.us-east-1.amazonaws.com/Prod



\---

## Create a Note

**POST /notes**

Creates a new note.

Example:

&#x20;   curl -X POST "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes" -H "Content-Type: application/json" -d "{\\"content\\":\\"My first cloud note\\"}"



\---

## Retrieve a Note

**GET /notes/{id}**

Fetches a note using its ID.

Example:

&#x20;   curl "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID"



\---

## Update a Note

**PUT /notes/{id}**

Updates the content of an existing note.

Example:

&#x20;   curl -X PUT "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID" -H "Content-Type: application/json" -d "{\\"content\\":\\"Updated note content\\"}"



\---

## Delete a Note

**DELETE /notes/{id}**

Deletes a note by ID.

Example:

&#x20;   curl -X DELETE "https://YOUR\_API\_ID.execute-api.YOUR\_REGION.amazonaws.com/STAGE/notes/YOUR\_NOTE\_ID"



\---

## Deployment

Build the application:

&#x20;   sam build



Deploy the infrastructure:

&#x20;   sam deploy



\---

## Monitoring

**Amazon CloudWatch Logs** are used to monitor Lambda execution and
troubleshoot API behavior during development and testing.

\---

## What I Learned

* How to build a serverless REST API using AWS services\\
* How Lambda integrates with API Gateway to process HTTP requests\\
* How DynamoDB stores and retrieves NoSQL data\\
* How to deploy infrastructure using **AWS SAM**\\
* How to debug and monitor serverless applications using
**CloudWatch**

\---

## Architecture Diagram

AWS\_serverless\_API\_architecture.jpg



