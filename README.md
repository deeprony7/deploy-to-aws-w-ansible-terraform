# Deploying to AWS with Terraform and Ansible

* Lets start by setting up S3 backend so we can persist Terrafrom state
```aws s3api create-bucket --bucket <bucket_name>```
OR
```aws s3 mb s3://<bucket_name> --profile <profile_name>```

* Set up backend.tf