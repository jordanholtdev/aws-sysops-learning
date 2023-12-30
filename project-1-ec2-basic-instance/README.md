# EC2 Instance

## Overview

Launch an EC2 instance with basic configurations, such as a specific Amazon Machine Image (AMI), instance type.

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj1Ec2Stack \
 --template-body file://ec2-instance-template.yaml \
 --parameters file://parameters.json
```
