## Create and configure the API Gateway

Before starting once more, it is worth recalling what API Gateway is.

See how AWS defines it:

*Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. APIs act as the "front door" for applications to access data, business logic, or functionality from your backend services. Using API Gateway, you can create RESTful APIs and WebSocket APIs that enable real-time two-way communication applications.*

> https://aws.amazon.com/api-gateway/

The definition explains very well what API Gateway is. Just remember that API Gateway allows you to create and use APIs.

### Create a REST API using API Gateway

First, go to API Gateway and **Build** a REST API:

![Build REST API](images/build-rest-api.png ':size=200')

Here, choose to create a *New API* of type *REST*. Give the API a suitable name (*SendingAPI* in this example) and create the API:

![REST API Creation](images/rest-api-creation.png ':size=900')

Once the API is created, click on the **Actions** button and select **Create Resource**:

![Create Resource](images/create-resource.png ':size=200')

Enter the name of the resource (here *sending*) and create the resource:

![Resource Configuration](images/resource-configuration.png ':size=700')

Once the resource is created, click on the **Actions** button and select **Create Method**

![Create Method](images/create-method.png ':size=200')

A field will appear, where the *POST* method should be selected since the purpose will be to publish the data from the website to the API.

When setting up the POST method, choose *Lambda Function* as the **Integration type**, enter the newly created REST API Handler (*restApiHandler*) in the **Lambda Function** field, and do NOT forget to **Use Lambda Proxy Integration**:

![POST Setup](images/post-setup.png ':size=700')

A window will appear asking to add permissions to the Lambda Function, click on **OK**:

![Add Permissions](images/add-permissions.png ':size=700')

The method is now created and points to the Lambda function *restApiHandler.py*, so at each POST method from the website, the API Gateway will receive the data and pass it directly to the REST API Handler. 

All that remains is to deploy the API, doing **Action** -> **Deploy API**:

![Deploy API](images/deploy-api.png ':size=200')

Make a *[New Stage]*, and choose the **Stage name** of your choice (*sendingStage* in this example):

![Deployment Stage](images/deployment-stage.png ':size=500')

The API is deployed in the newly created stage. It will now be possible to send data to API Gateway via the **Invoke URL** of the stage:

![Invoke URL](images/invoke-url.png ':size=1000')

The **Invoke URL** is ready. All that remains to be done is to create the website *index.html* on which the data will be entered, as well as the script *formToApi.js* that will send the data to the Invoke URL.

### [Code a website and upload it to S3](https://github.com/OmarKhalil401/Serverless-Notification-Sending-Application/blob/main/7-S3/README.md)