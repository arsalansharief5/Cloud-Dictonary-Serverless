Cloud Dictionary

A fully serverless dictionary app hosted on AWS Amplify, with backend powered by AWS Lambda, API Gateway, and DynamoDB.
Search for any word and get its meaning instantly — all in the cloud, no servers to manage.

⸻

<<<<-About the Project->>>>

• Static frontend hosted on AWS Amplify

• Backend API using API Gateway + Lambda (Python)

• DynamoDB stores words and definitions

• Fully serverless and scalable


⸻

<<<<-Features->>>>

• Search for any word

• Fully serverless backend

• DynamoDB stores dictionary entries

• Frontend hosted on AWS Amplify


⸻

<<<<-Architecture Overview->>>>

Browser →  AWS Amplify  → API Gateway → Lambda → DynamoDB



Components:

• Frontend: Static HTML/CSS/JS hosted on Amplify

• API Gateway: HTTP API exposing /dictionary?word=cloud

• Lambda Function (Python): Reads definitions from DynamoDB

• DynamoDB: Stores words and their meanings


⸻

<<<<-How It Works->>>>

1. User types a word in the Amplify-hosted frontend

2. Frontend calls API Gateway endpoint

3. API Gateway triggers Lambda function

4. Lambda fetches word from DynamoDB

5. Definition returned as JSON

6. Frontend displays the result

⸻

<<<<-Tech Stack->>>>

• Frontend:-> HTML, CSS, JavaScript

• Hosting:-> AWS Amplify

• API:-> AWS API Gateway (HTTP API)

• Backend:-> AWS Lambda (Python)

• Database:-> Amazon DynamoDB


⸻

<<<<-Lambda Function (Python)->>>>


import json
import boto3

dynamo = boto3.resource("dynamodb")
table = dynamo.Table("Dictionary")

def lambda_handler(event, context):
word = event.get("queryStringParameters", {}).get("word")

if not word:
return {"statusCode": 400, "body": json.dumps({"error": "Missing word"})}

try:
response = table.get_item(Key={"word": word})

if "Item" not in response:
return {"statusCode": 404, "body": json.dumps({"definition": None})}

return {"statusCode": 200, "body": json.dumps(response["Item"])}
except Exception as e:
return {"statusCode": 500, "body": json.dumps({"error": str(e)})}

⸻

<<<<-Current Status->>>>

• Fully serverless dictionary app

• Frontend hosted on AWS Amplify

• Backend: API Gateway → Lambda → DynamoDB

• CORS configured for smooth frontend-backend communication

• Works instantly on search queries


⸻

<<<<-Future Enhancements->>>>

• Add multiple definitions per word

• Add pronunciation/audio

• Add user login via Cognito

• CI/CD deployment with Amplify auto-sync

• CloudFront for global caching 


⸻

<<<<-Contributing->>>>


>>Open issues for suggestions or bugs.

⸻

