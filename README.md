# aws-s3-website

CloudFormation template for an S3 backed website.

**Note:** this template is still WIP

## Input & Output Parameters

The template only requires a bucket name as input parameter.

The template's output is the `Arn` of the bucket serving the static website content, as well as the HTTP & HTTPS endpoints.

## Resources

The CloudFormation template creates two buckets:

- Public bucket serving the static website
- Private bucket for the [Server Access Logs](https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerLogs.html)

The access logs are kept for 180 days and transitioned to Glacier after 30 days.
