# Step Functions Example
This is an example of creating, deploying and incoking AWS Step Functions created with the Serverless Framework. This time we will also add an AWS API Gateway.


## Prerequisites

* You have made you AWS access and secret key available through a provided method, like storing them in the ~/.aws/credentials file or export them into environment variables
* You need to install Node.js  with a minimum version of 6.5.0 
* Then you need to install the serverless CLI with `sudo npm install -g serverless`
* `npm install`


## Deploy

* `serverless deploy -v`


## Test

* Now you could invoke the Step Function with `serverless invoke stepf -n hellostepfunc1` if everything went fine. We should see the output: `ciao world!`
* This time we also have an API Gateway which calls the Step Function, so we could curl the API Gateway endpoint to see if everything went fine. You can find the respective URL in the output of `serverless deploy -v`. In difference to using to `serverless invoke` command you will not see the `ciao world!` but only an info the Step Functions ARN and the execution date, which indicates it was executed.


## Undeploy

* `serverless remove`