# Serverless-Web-Application
Deploying a serverless web app by using AWS Amplify,Aws cognito,Amazon API Gateyay,Lambda and Dynamo DB

In This project I will create a serverless web app for requesting unicorn ride from aws example web site http://www.wildrydes.com/ show the where are the unicorns and take a request from users for ride the unicorns and show the closest unicorn.Also with the app user can register the service and log in.I will use Amplify for static web hosting include html,css,javascript and image files,Cognito for user management,AWS API gateway for restful apı and dynamodb for serverless backend.

Start to project with creating a git repo in aws.I use CodeCommit for this.To use CodeCommit have to set up git credential first.Then I can clone to repo and dowland necessery files from S3 bucket which provided from aws itself.I will also add this files to github repo for showing but I dont create this files.Files provided from AWS and I use them for project.
![gitcommit repo](docs/assets/Screenshot%20from%202023-04-10%2018-19-03.png)
![gitcommit repo](docs/assets/Screenshot%20from%202023-04-10%2018-19-18.png)

Then I use AWS amplify for static wb site hosting.Connect my repo in gitcommit to amplify for frontend hosting.Then making configuration at the end.Then amplify deploy frontend.
![amplify](docs/assets/Screenshot%20from%202023-04-10%2020-14-04.png)
![website](docs/assets/Screenshot%20from%202023-04-10%2020-14-17.png)

After couple of minutes building finish and now We can see the the application frontend.When I make a change in html or css or any code ampfy updating the appllication.Now I will make some changes in frontend.Then amplify update and build again.
![website](docs/assets/Screenshot%20from%202023-04-10%2020-28-40.png)

After this step I will use Amazon Cognito for creating user pool.User can sign in and log in to application through Amazon Cognito.Then I configure  and create a cognito user pool.Then update to config file and replace the cognito userpoolıd and userpoolclient ıp with my values.Lastly I will test my user pool by try to sign in and login to application.
![cognito1](docs/assets/Screenshot%20from%202023-04-10%2020-50-08.png)
![cognito2](docs/assets/Screenshot%20from%202023-04-10%2020-50-23.png)
Then update to config file and replace the cognito userpoolıd and userpoolclient ıp with my values.Lastly I will test my user pool by try to sign in and login to application.
![verify1](docs/assets/Screenshot%20from%202023-04-10%2021-12-20.png)
![website](docs/assets/Screenshot%20from%202023-04-10%2021-29-30.png)
![website](docs/assets/Screenshot%20from%202023-04-10%2021-29-35.png)

This part of project I will use aws lambda and amazon dnamodb for build a backend for application.This backend handling request of web application.Users request of this app is customers want unicorns to their location and javascript running in browser have to invoke for fulfilling this request.I will use aws lambda for this.Lambda function invoke everytime a user request a unicorn.Lambda function select a closest unicorn in the dynamodb table then frontend app show the user to unicorn.

First start with create a dynamodb table.
![dynamodb](docs/assets/Screenshot%20from%202023-04-10%2021-56-39.png)
Then create a IAM role my lambda function.This role gives a permisson to lambda function to write cloudwatch logs and put items to dynamodb table.Give to necessary policies to role and create the role I will attach this role to lambda function.
![ıamrole](docs/assets/Screenshot%20from%202023-04-10%2022-00-51.png)
Second I need to create a lambda function for processing apı request and dispatch unicorns.I use lambdafunction.js for lambda function.
![lambda](docs/assets/Screenshot%20from%202023-04-10%2022-12-45.png)
Then testing lambda function functionality
![testing](docs/assets/Screenshot%20from%202023-04-10%2022-19-01.png)
Now it works.
![testing2](docs/assets/Screenshot%20from%202023-04-10%2022-19-30.png)


























