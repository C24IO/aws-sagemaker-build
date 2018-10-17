# AWS SageMaker Build
Creates a CloudFormation template that uses AWS StepFunctions to automate the building and training of Sagemaker custom models based on S3 and GitHub events

## setup
```shell
node -e "console.log('Running Node.js ' + process.version)"
. ~/.nvm/nvm.sh
nvm install 8
npm install aws-sdk lodash
npm install
npm run up
```
create an s3 bucket. [instructions](https://docs.aws.amazon.com/AmazonS3/latest/dev/create-bucket-get-location-example.html). open up config.json and set templateBucket to the name of your s3 bucket.

## Stack Management
```shell
npm run up #launches stack with default paramters
```
```shell
npm run update #updates the launched stack
```
```shell
npm run down #shuts down stack
```

template is written to /cloudformation-template/build/template.json

## Rough

Use Cloud 9
node -e "console.log('Running Node.js ' + process.version)"
nvm install 8
npm install aws-sdk lodash uglify-es github
npm install -g express-generator
npm install -g npm@latest
npm install npm@latest
npm run up

create S3 bucket and then change - "templateBucket":"aws-sagemaker-build-prod"


## Todo

1) Remove need for npm to create a cloudformation tempalte
2) Can we have a cloudformation template directly?
3) Move from npm to Go/Python?
4) Drive this using a frontend like Hortonworks Cloudbreak?
5) Possiblity to move to Jenkins or integrate other CI/CD?
6) Model versioning?
7) Data versioning?
8) Keep up with velocity of changes of SM Platform?
9) Dockerize npm?
10) Why remember state of last CloudFormation Template produced? 
11) Second run fails without good errors
12) This is a meta service - need 1 step?

## Race

1) First deployment fails at - FailBuildTraining
2) Stack Delete Failed - EndpointConfigClear	2018/10/17/[$LATEST]f21329d3f7c8417d9c4f918a33ebe97f
3) Stack Delete Failed - ModelClear	2018/10/17/[$LATEST]3b2d4719ed5f4e9faf94f88ba79bab62