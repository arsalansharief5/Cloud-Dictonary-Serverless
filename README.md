# Cloud-Dictonary
The Cloud Dictionary App is a fully serverless application built using AWS Amplify, Lambda, API Gateway, and DynamoDB. The project allows users to search for word meanings through a simple web interface, where all data is stored and managed in the cloud.

The frontend is deployed using AWS Amplify Hosting, providing a fast and scalable UI. When a user searches for a word, the request is sent to Amazon API Gateway, which triggers an AWS Lambda function. The Lambda function processes the request, retrieves the word definition from DynamoDB, and returns it to the frontend. Users can also add new words and meanings, enabling dynamic expansion of the dictionary.

This project demonstrates how to combine multiple AWS services to create a real-world, cost-efficient serverless application with zero-maintenance infrastructure. It highlights key concepts such as API development, event-driven computation, NoSQL database design, IAM roles, and cloud deployment workflows.

The Cloud Dictionary App is cloud-native application using AWS serverless technologies while creating a functional, scalable, and user-friendly web application.
What This Project Does





About This Project:



<<<<<<<- The app lets users ->>>>>>>

1. Search for word meanings

2. Add new words and definitions

3. Access everything through a clean cloud-hosted web interface




<<<<<- How it works ->>>>>

1. The frontend is hosted using AWS Amplify.

2. When you search a word, the browser sends the request to API Gateway.

3. API Gateway triggers a Lambda function, which fetches the meaning from DynamoDB.

4. The result is sent back to the user instantly.



<<<<<- Tech Stack ->>>>>

1. AWS Amplify – Frontend hosting

2. AWS Lambda – Backend logic

3. API Gateway – Creates the REST API

4. DynamoDB – Stores words & meanings

5. JavaScript / HTML / CSS – Simple client UI




<<<<<- Why I built this ->>>>>

I wanted to create a cloud project that is practical and meaningful, while showing how different AWS services connect to form a complete full-stack application. This project helped me learn:

1. How serverless apps are structured

2. How APIs work with Lambda

3. How to store and fetch data from DynamoDB

4. How to deploy a real app using Amplify





<<<<<- Features I wll add later ->>>>>

1. User authentication

2. Update/Delete words

3. Search suggestions

4. Logging & monitoring with CloudWatch

5. CI/CD integration
