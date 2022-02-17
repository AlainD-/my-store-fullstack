# Dependencies

* **credentials**: An Amazon IAM credentials must be created to allow access to the Elastic Beanstalk CLI: Attach the group "AdministratorAccess" to the group of that IAM user.
* **database**: In order to install the application, an Amazon RDS Postgres must be created. Even though the application should be compatible with newer version of Postgres, it has been developped and tested with Postgres version 12, and there is no guarantie provided for it to work with another version of Postgres. Inbound security rules must be set to allow `0.0.0.0/0` for all traffic.
* **node**: NodeJS 14 and NPM version 6. The AWS Elastic Beanstalk environment must be created and set for a NodeJS application version 14.
* **bucket**: An Amason S3 bucket must be created and configured for web hosting: **Static website hosting** must be **Enabled**. The S3 bucket permissions must be set so that is accessible with read permissions from the Internet. The following Bucket Policy can be used an adapted to the bucket in question:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::my-store-alaind/*"
        }
    ]
}
```
