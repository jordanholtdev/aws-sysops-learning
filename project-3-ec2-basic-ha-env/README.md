# Basic HA Environment

## Overview

-   create a VPC with four subnets
-   attach IG
-   configure route tables: two public subnets and two private
-   EC2 instance with public IP and public connectivity
-   create security group
-   create auto scaling group
-   create ELB
-   create listener
-   create CloudWatch metric alarm with action that scales out if CPU > 90%

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj3HaEnv \
 --template-body file://basic-env.yaml \
 --parameters file://parameters.json
```
