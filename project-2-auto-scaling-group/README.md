# Auto Scaling Group Template

Set up an Auto Scaling Group, using a step scaling policy with a CloudWatch Alarm that automatically scales out when CPU utilization is greater than 90%. Instances are load balanced using an ALB.

## Overview

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj2ASG \
 --template-body file://asg.yaml \
 --parameters file://parameters.json
```
