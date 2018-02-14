# aws-s3-website

CloudFormation template for an S3 backed website.

**Note:** this template is still WIP

## Parameters

- Bucket Name

The following parameters are optional and used to further distinguish resources from multiple stacks, e.g. to drive customer cost analysis.

- Owner
- Support
- Use Case

## Resources

The CloudFormation template creates two buckets:

- Public bucket serving the static website
- Private bucket for the [Server Access Logs](https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerLogs.html)

The access logs are kept for 180 days and transitioned to Glacier after 30 days.
