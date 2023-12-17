# Auto Scaling Group Template

Set up an Auto Scaling Group that automatically adjusts the number of instances based on traffic. Include an Amazon Elastic Load Balancer (ELB) to distribute traffic.

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
