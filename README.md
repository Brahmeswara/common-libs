# NodeJS Common Libraries Layer
This repo contains the package.json with all the required libraries. Idea here
is to make all the related librries as one layer for use in lambda functions.

It is **assumed that** you are familiar with AWS and have necessary pre-requisites installed already. This uses AWS SAM client to package and deploy the Lambda Layer code.


Note, these are pushed into AWS CodeArtifact repo (and not to the npm repo).
You have all the files available in git repo for understanding purposes.

Code here uses an S3 bucket to create the AWS cloudformation templates. for your case, change the
S3 bucket as needed. 

## Step 1: Building Layer 

Execute the the following to have the layer code built.

    npm run build-production

## Step 2: Deploying to AWS

Execute the following to have he layer deployed in AWS Lambda.

    npm run aws-deploy

Refer to the package.json for details on how the above commands are setup. 