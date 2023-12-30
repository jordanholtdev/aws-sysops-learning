# Configure S3 Buckets

## Overview

Basic S3 Bucket

-   Public Access Blocked
-   Encryption using SSE-S3 with Bucket Key enabled

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj5S3 \
 --template-body file://basic-s3.yaml \
 --parameters file://parameters.json \
```
