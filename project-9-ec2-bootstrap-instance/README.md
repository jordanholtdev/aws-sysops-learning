# EC2 Bootstrap Instance

## Overview

-   Bootstrap a single EC2 instance using the `cfn-init` to read metadata and `cfn-signal` to return the status of the call to `cfn-init`. In this case the file from the metadata and init package are being installed during launch via a bash script in `userdata`. The `CreationPolicy` attribute prevents the status from reaching complete until a success signal is received or a timeout period of 5mintues is exceeded.

## CloudFormation Deployment

1. Create a `parameters.json` file and include the necessary parameters for your environment.
2. Create a Stack using the AWS CLI

```bash
 aws cloudformation create-stack \
 --stack-name proj9Ec2Stack \
 --template-body file://ec2-bootstrap.yaml \
 --parameters file://parameters.json
```
