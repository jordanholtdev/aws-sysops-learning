# Configure S3 Buckets

## Overview

Basic S3 Bucket

-   Public Access Blocked
-   Encryption using SSE-S3 with Bucket Key enabled
-   Lifecycle configuration rule to transition to Standard IA after 30 days
-   IA archive configuration to move objects tagged with `opt-in-archive: true` from IA to Deep Archive Access after 180 days

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj6S3 \
 --template-body file://ia-s3.yaml \
 --parameters file://parameters.json \
```
