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

## Helpful CLI commands for testing

Calulate the SHA-256 checksum of an object before upload to verify integrity

```bash
sha256sum somefile.json | awk '{print $1}' | xxd -r -p | base64
```

Upload an object to a bucket using the `PutObject` api

```bash
aws s3api put-object \
--bucket BUCKET-NAME \
--key dir-1/somefile.json \
--body somefile.json \
--storage-class STANDARD \
--metadata visibility=private,version=1,category=reports,source=sensorA,document-type=json \
--tagging "Environment=test&Owner=sysops&Project=sysops" \
--checksum-algorithm SHA256 \
--checksum-sha256 "filesha256checksum"

```
