# AWSIMPAIRED
Lambda_Bash
List all the impaired instances from all regions and all account using AWS CLI and Bash Script

Documentation
Given Bash script . List all the Impaired Instances from all regions and all AWS accounts , which are specified in RoleARN Env var .

Bootstrap

Using a custom runtime

To use a custom runtime, set your function's runtime to provided. The runtime can be included in your function's deployment package, or in a layer.

Example function.zip container two files

bootstrap

function.sh

If there's a file named bootstrap in your deployment package, Lambda runs that file. If not, Lambda looks for a runtime in the function's layers. If the bootstrap file isn't found or isn't executable, your function returns an error upon invocation.

Bootstrap File
You can implement an AWS Lambda runtime in any programming language. A runtime is a program that runs a Lambda function's handler method when the function is invoked. You can include a runtime in your function's deployment package in the form of an executable file named bootstrap.
https://docs.aws.amazon.com/lambda/latest/dg/runtimes-custom.html

Lambda IAM Role
Lambda IAM Permissions Where Lambda Function is Created:

Amazon EC2 ReadOnly Access
Amazon SES Permissions
Lambda Basic Execution Permissions
Assume Policy Pass STS assume policy
Lambda IAM Permissions for Test account

Amazon EC2 ReadOnly Access
Install AWSCLI
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

Environment Variables
To run this project, you will need to set the following environment variables in your bashscript

RoleARN : List of Arns

OUT2 : To switch roles and send AWS SES Mail .

OUT : Assume Role .

Access keys consist of an access key ID and secret access key, which are used to sign programmatic requests that you make to AWS

AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

Specifies an AWS session token used as part of the credentials to authenticate the user

AWS_SESSION_TOKEN

ConfigName : Lit all the imparied instances

sample_data: AWS SES mail body , container all details of imparied Instances .
