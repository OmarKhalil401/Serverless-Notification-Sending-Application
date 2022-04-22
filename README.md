
# Serverless Notification Sending Application

Sending Email and SMS from a Website using AWS Serverless services.

Through this project, you will be able to send an email or a SMS from a website using AWS services. Along the way, you will learn how to:

* Execute email and SMS sendings from a website using S3, API Gateway and Lambda.
* Manage email and SMS sendings using Step Functions.
* Create and send an email with AWS using SES and Lambda.
* Create and send a SMS with AWS using SNS and Lambda.

**Take a closer look at the infrastructure deployed with this project:** 

## Architecture Diagram

![Project Diagram](https://i.imgur.com/gVvjpmU.png)

##  Project Roadmap

Navigate through the project's folders to learn more about each step and compelete the project.

[1. Create a Lambda Role](/LambdaRole/README.md) 

2. Send Email using SES and Lambda

3. Send SMS using SNS and Lambda

4.  Create and Manage how to send Notifications using Step Functions

5. Create the REST API Handler using Lambda

6. Create and configure the API Gateway

7. Code a website and upload it to S3

8. Create and configure the API Gateway

<HR>

## Project FAQ

### How much would deploying this project cost? 

**Less than $1**

This project will only be using tools supported by the Free Tier. <br/>
The costs generated by the project come from the SNS service, more exactly the SMS Pricing. <br/>
See more here:[ AWS SNS Pricing ](https://aws.amazon.com/sns/sms-pricing/)

### What Tool are going to be used in this project?

**AWS**

    S3
    API Gateway
    Lambda
    Step Functions
    SNS
    SES

**Programming**

    python
    js & json
    html

### What are the free Tier Conditions of this project?

    S3:
        5 GB of free storage
        20,000 free GET requests & 2,000 free PUT requests

    API Gateway:
        1 Million API Calls Received

    Lambda:
        1,000,000 free requests per month
        Up to 3.2 million seconds of compute time

    Step Functions:
        4,000 state transitions

    SNS:
        1,000,000 Publishes
        100,000 HTTP/S Deliveries
        1,000 Email Deliveries

    SES:
        62,000 Outbound Messages
        1,000 Inbound Messages

## Documentation

[AWS Lambda](https://aws.amazon.com/lambda/)

[boto3 SDK](https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html)

[AWS SES](https://docs.aws.amazon.com/ses/)

[AWS SNS](https://docs.aws.amazon.com/sns/index.html)

[AWS S3](https://docs.aws.amazon.com/s3/index.html)

[AWS Step Functions](https://aws.amazon.com/step-functions/)

[AWS API Gateway](https://aws.amazon.com/api-gateway/)

[What is a REST API](https://www.youtube.com/watch?v=lsMQRaeKNDk)









