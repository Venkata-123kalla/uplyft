Lambda Function for Processing S3 Events and Storing Data in DynamoDB
Overview
This AWS Lambda function listens for S3 events when a file is uploaded to an S3 bucket. Upon receiving the event, the function reads a CSV file from the S3 bucket, processes its contents, and stores the data in a DynamoDB table named Customer. The data includes details such as Day, Customers, Gross, and Expenses.

Requirements
Before using this Lambda function, ensure that the following AWS services and resources are in place:

Amazon S3: The S3 bucket stores the customer CSV file that triggers the Lambda function.
AWS Lambda: The Lambda function executes the Python code to process the S3 event.
Amazon DynamoDB: A DynamoDB table named Customer is used to store the parsed data from the CSV file.
IAM Role: The Lambda function must have permissions to:
Read objects from the S3 bucket.
Write items to the DynamoDB table.
Prerequisites
Boto3: The AWS SDK for Python (Boto3) is used to interact with S3 and DynamoDB.
CSV Format: The customer data is stored in CSV format. Each line in the file must have the following fields: Day, Customers, Gross, and Expenses.
