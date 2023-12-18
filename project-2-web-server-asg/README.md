# Web server auto scaling group

## Overview

This is an auto scaling group for web servers with Apache installed. This ASG uses a step scaling policy with a CloudWatch Alarm that automatically scales out when CPU utilization is greater than 90%. Instances are load balanced using an ALB.

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj2ASG \
 --template-body file://asg.yaml \
 --parameters file://parameters.json
```
