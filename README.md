# GoDigitalInternTask


# AWS Data Pipeline

This project demonstrates a data pipeline using AWS services. It reads data from an S3 bucket, processes it using a Lambda function, and stores it in an RDS database. If the RDS database is unavailable, the data is pushed to an AWS Glue database.

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
