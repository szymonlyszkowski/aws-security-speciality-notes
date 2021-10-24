## CloudTrail

* CloudTrail logs are **encrypted** by default. No need to use KMS to encrypt bucket where they are stored.
* CloudTrail by default are **NOT** enabled for your AWS Organization. In order to enable it use **master account** & apply CloudTrail to organization. There is no need to enable it for each OU separately. Details in [docs](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/creating-an-organizational-trail-in-the-console.html):
  * When creating trail, trail logs **all** regions (recomended as best practice)
  * Specify S3 bucket to deliver trail (create a new one or use existing)
  * Specify which events to log: **Read, write, both**
