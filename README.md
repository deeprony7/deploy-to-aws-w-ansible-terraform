# Deploying to AWS with Terraform and Ansible

* Lets start by setting up S3 backend so we can persist Terrafrom state
```aws s3api create-bucket --bucket <bucket_name>```

* Set up backend.tf