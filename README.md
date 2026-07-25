# GoDigitalInternTask


# AWS Data Pipeline

This project demonstrates a data pipeline using AWS services. It reads data from an S3 bucket, processes it using a Lambda function, and stores it in an RDS database. If the RDS database is unavailable, the data is pushed to an AWS Glue database.

## Architecture
<img width="1536" height="1024" alt="lab2" src="https://github.com/user-attachments/assets/338f76e6-53ee-4fc4-8170-8d8f9ad77da9" />


## Files
- `app.py`: Python script to read data from S3 and push to RDS or Glue.
- `Dockerfile`: Dockerfile to create a Docker image for the Python script.
- `main.tf`: Terraform configuration to create AWS resources.
- `variables.tf`: Terraform variables for resource configuration.
- `outputs.tf`: Terraform outputs for resource information.
- `jenkinsfile`: Jenkins pipeline script to automate the CI/CD process.

## Usage
1. Clone the repository.
2. Add the necessary AWS credentials to your Jenkins server.
3. Configure the Jenkins pipeline using the `jenkinsfile`.
4. Run the Jenkins pipeline to build and deploy the project.



##Screenshots:

1) Final RDS table called "names" which is storing all the names uploaded in csv in S3 bucket

![Screenshot 2024-06-16 151757](https://github.com/Its-Lord-Stark/aws-data-pipeline/assets/126385754/480f24e0-fdfe-4d83-8942-2a39a5a10290)


3) Lambda Function with S3 upload trigger

![Screenshot 2024-06-16 152010](https://github.com/Its-Lord-Stark/aws-data-pipeline/assets/126385754/b53c6f46-68f2-4005-b510-021a1068c6d9) 

3)Docker Image build for lambda_function_payload.zip that have lambda function and required ependancies like pymysql and boto3

![Screenshot 2024-06-16 151544](https://github.com/Its-Lord-Stark/aws-data-pipeline/assets/126385754/3bc77baa-5565-43ba-a383-14f5933e10cb)

4)ECR Repo with Docker images pushed

![Screenshot 2024-06-16 152010](https://github.com/Its-Lord-Stark/aws-data-pipeline/assets/126385754/04940821-2607-47e7-ac9f-d139be6de220)

5)RDS Instance named mydb

![Screenshot 2024-06-16 150529](https://github.com/Its-Lord-Stark/aws-data-pipeline/assets/126385754/199bbbfd-d42c-4d86-a558-f991d9328edf)

6)Unique named s3 bucket with notification to lambda function

![Screenshot 2024-06-16 150450](https://github.com/Its-Lord-Stark/aws-data-pipeline/assets/126385754/0288eb4f-4771-415c-986c-a0c30c71f662)

7)The pipeline building(I know 60 builds isnt good but i gave my all)

![Screenshot 2024-06-16 152656](https://github.com/Its-Lord-Stark/aws-data-pipeline/assets/126385754/de685fa6-3589-4e67-891b-ee2ddccbfe71)



8)Finally Cloudwatch logs screenshot of lambda function where there is no error

![Screenshot 2024-06-16 150536](https://github.com/Its-Lord-Stark/aws-data-pipeline/assets/126385754/21784ff7-070a-43a2-9fc4-84c03841ff66)





