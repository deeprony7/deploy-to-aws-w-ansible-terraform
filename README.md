# Deploying to AWS with Terraform and Ansible

* Run `aws configure --profile <profile_name>` to set up your credentials. You need the access and the secret key for this.
  *PS: I am using profile_name as demo*
* Lets start by setting up S3 backend so we can persist Terrafrom state
```aws s3api create-bucket --bucket <bucket_name> --profile <profile_name>```
OR
```aws s3 mb s3://<bucket_name> --profile <profile_name>```

* Set up backend.tf with the bucket name and key to use to store the data
* Set up network_setup.tf 


### Create an HTTP API by using the AWS CLI

```
aws apigatewayv2 create-api --name my-api --protocol-type HTTP --target arn:aws:lambda:us-east-2:123456789012:function:function-name
```