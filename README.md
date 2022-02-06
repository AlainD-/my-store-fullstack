# My-Store Full-Stack

This project explains the fullstack application of the [StoreFront API](https://github.com/AlainD-/storefront-api) backend and the [My-Store](https://github.com/AlainD-/my-store) frontend.

## Backend

* Deployed url (Elastic Beanstalk): [http://storefrontapi-env-1.eba-xpkyym8v.us-east-1.elasticbeanstalk.com/](http://storefrontapi-env-1.eba-xpkyym8v.us-east-1.elasticbeanstalk.com/)

## Frontend

* Deployed url (S3 Bucket): [http://my-store-alaind.s3-website-us-east-1.amazonaws.com/](http://my-store-alaind.s3-website-us-east-1.amazonaws.com/)

## Important Notice

The backend and the frontend repositories are configured to automatically build and deploy on AWS with circleCI.
The instructions given here are to be used to manually trigger an automatic build and deployment of the full stack at once.

## Installation

* Clone the [StoreFront API](https://github.com/AlainD-/storefront-api) backend in the current directory
* Clone the [My-Store](https://github.com/AlainD-/my-store) frontend in the current directory
* Install the backend by running the command in the terminal: `npm run backend:install`
* Install the frontend by running the command in the terminal: `npm run frontend:install`

## Deploy

* Deploy backend by running the command in the terminal: `npm run backend:deploy`
* Deploy the frontend by running the command in the terminal: `npm run frontend:deploy`

## Documentation

The deployment proofs consist in screenshots located in the [screenshots](./screenshots) folder.

### Backend deployment in AWS Elastic Beanstalk

* AWS Beanstalk configuration
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/aws-eb-config.png)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/aws-iam-user.png)
* CircleCI configuration
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/storefront-api-circle-ci-project-settings-environment-variables.png)
  * [.circleci/config.yml](https://raw.githubusercontent.com/AlainD-/storefront-api/master/.circleci/config.yml)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/storefront-api-circle-ci-workflow.png)
* Deployed successfully
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/storefront-api-beanstalk-deploy-success.png)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/storefront-api-aws-eb-deploed-healthy.png)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/storefront-api-circle-ci-deploying-success-with-eb-cli.png)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/storefront-api-circle-ci-deploy-latest-success.png)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/storefront-api-tag-success.png)

### Frontend deployment in AWS S3 bucket

* AWS S3 Bucket configuration
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/aws-s3-bucket-webhosting-config.png)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/aws-s3-bucket-permissions-config.png)
* CircleCI configuration
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/my-store-circle-ci-environment-variables.png)
  * [.circleci/config.yml](https://raw.githubusercontent.com/AlainD-/my-store/master/.circleci/config.yml)
* Deployed successfully
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/my-store-s3-deploy-success.png)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/my-store-circle-ci-deploy-success.png)
  * ![MyStore](https://raw.githubusercontent.com/AlainD-/my-store-fullstack/master/screenshots/my-store-tag-success.png)

## License

[License](LICENSE)

## Authors

* **Alain D'EURVEILHER** - _Initial work_ - [AlainD.](https://github.com/AlainD-)
