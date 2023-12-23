# Configure S3 Buckets

## Overview

Primary S3 bucket with versioning and replication enabled to a secondary S3 bucket.

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj4S3 \
 --template-body file://s3.yaml \
 --parameters file://parameters.json \
 --capabilities CAPABILITY_NAMED_IAM
```
