# Basic VPC

This is a basic VPC with corresponding resources that could be used for a development / test environment.

## Overview

VPC

-   1 AZ
-   2 Subnets
    -   1 Public Subnet
    -   1 Private Subnet
-   IG
-   1 Public NAT Gateway
-   2 route tables
    -   public route table
    -   private route table
-   1 SG

TODO:

-   [ ] Add NACLs

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj8S3 \
 --template-body file://vpc-basic-dev.yaml \
 --parameters file://parameters.json
```

## Helpful CLI commands for testing
