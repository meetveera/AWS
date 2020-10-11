## Technology Stack

Backend - Node JS<br>
Database - Postgres<br>
Server - Postman<br>

## Build Instructions

Node server.js<br>
Api calls on postman<br>

## Deploy Instructions

git add --all<br>
git commit<br>
git push<br>

## Running Tests

Unit Integration: Email validation<br>

## CI/CD

Use curl command to deploy application<br>
CircleCi will fettch application from repository Github and create API call for CodeDeploy<br>
CodeDeploy will deploy the apllication to individual instances<br>

## This application is build using nodejs and mysql server. To run this application locally, following are the steps:

- Clone and download this application from github using SSH format link
- The SSH key is set and will not ask for username or password
- Go on the terminal in the local repository folder and give command, node server.js
- This will run the application on localhost:3000 which carries out REST API Call; POST, PUT, GET and DELETE on the Bill Tracking Application
- Deploy commands for web application are :
- export AWS_PROFILE=prod
- git checkout -b branch
- git status
- git add .
- git commit -m "YOUR COMMIT MESSAGE"
- git push

## After sshing into the new instance

- ssh -i ~/.ssh/keypairprodus2 ubuntu@"EC2publicIP"
- scp the webapp into the new instance
- scp -r webapp ubuntu@EC2PrivateIP:~/

## Inside the webapp follow these commands-

## Install nodejs with these commands inside EC2

- sudo apt-get install curl
- curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
- sudo apt-get install -y nodejs

## CI/CD

- The appspec.yml file is created in the root repository
- The codedeploy folder contains the applicationStop.sh, afterInstall.sh and applicationStart.sh file
- The application will be pushed into git branch.
- The web application is zipped and sent to S3 bucket.
- The complete CICD process is executed and the appplication runs on the EC2 instance without manually sshing into the EC2 instance

## CloudWatch

To calculate the number of times an api is called by the user and the time duration to get results
Installed cloudwatch-agent in AMI and linked the policies to it in cloudformation
Used winston to send logs to aws

## Jmeter folder containing jmx file added to webapp
