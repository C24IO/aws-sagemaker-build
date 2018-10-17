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
