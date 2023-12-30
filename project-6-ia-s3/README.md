# S3 Intelligent-Tiering basic example

## Overview

S3 Intelligent-Tiering basic example

-   Public Access Blocked
-   Encryption using SSE-S3 with Bucket Key enabled
-   Lifecycle configuration rule to transition to Intelligent-Tiering after 0 days.
-   Intelligent-tiering archive configuration to move objects tagged with `opt-in-archive: true` from IA to Deep Archive Access after 180 days

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj6S3 \
 --template-body file://it-s3.yaml \
 --parameters file://parameters.json \
```
