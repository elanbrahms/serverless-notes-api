# \# Serverless Notes API

# 

# \## Overview

##### A serverless REST API built with AWS Lambda, API Gateway, DynamoDB, and AWS SAM. The application supports full CRUD operations for notes.

# 

# \## Architecture

##### Client → API Gateway → Lambda → DynamoDB

# 

# \## AWS Services Used

##### \- AWS Lambda

##### \- API Gateway

##### \- DynamoDB

##### \- IAM

##### \- AWS SAM

##### \- CloudWatch

# 

# \## API Endpoints

##### \- POST /notes

##### \- GET /notes/{id}

##### \- PUT /notes/{id}

##### \- DELETE /notes/{id}

# 

# \## Example Requests



# \### Create Note

##### curl -X POST "..."

# 

# \### Get Note

##### curl "..."

# 

# \## Deployment

##### sam build

##### sam deploy

# 

# \## What I Learned

##### \- How to build a serverless API

##### \- How Lambda integrates with API Gateway

##### \- How DynamoDB stores NoSQL data

##### \- How to deploy infrastructure using AWS SAM



# \## Architecture Diagram

# !\[Architecture](AWS serverless API architecture.png)

