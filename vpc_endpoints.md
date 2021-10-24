## VPC Interface endpoint vs Gateway endpoint

**Gateway Endpoints** rely on creating entries in a route table and pointing them to private endpoints used for **S3 or DynamoDB**. Interface Endpoints use AWS PrivateLink and leverages the new Network Load Balancer capabilities.

* VPC Interface Endpoint == VPC Endpoint
* VPC Gateway Endpoint can connect to AWS DynamoDB or AWS S3
* S3 can be connected via VPC Interface endpoint. [How to choose between Interface & Gateway endpoint for S3](https://aws.amazon.com/blogs/architecture/choosing-your-vpc-endpoint-strategy-for-amazon-s3/)
