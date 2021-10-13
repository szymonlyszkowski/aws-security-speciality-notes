### AWS Lambda Permissions
* __Execution role__ - allows AWS Lambda to invoke actions on other AWS services aka service role
  * Send logs to CloudWatch
  * Upload trace data to AWS X-Ray

* __Resource-based__ policies
  * Allows **other** AWS services to invoke lambda function on your behalf
  * Grant usage permission to other AWS accounts on a per-resource basis

* __IAM based access__ - allow **IAM Users or Groups** to access Lambda
  * _AWSLambda_FullAccess_  – Grants **full access** to Lambda actions and other AWS services used to develop and maintain Lambda resources.
  * _AWSLambda_ReadOnlyAccess_ **read-only** access to

  * _AWSLambdaRole_ – Grants permissions to invoke Lambda functions.

*  __Resources & conditions__ - restrict the scope of a user's permissions by specifying resources and conditions in an IAM policy.

* __Permission Boundries__ -  limits the scope of the execution role that the application's template creates for each of its functions, and any roles that you add to the template
