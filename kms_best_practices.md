# AWS KMS

## KMS & IAM
  * IAM Policies usage within KMS
  * Key Policies
  * Cross account sharing keys
  * Encryption context
  * MFA for keys

## Detective controls
Making sure AWS KMS is properly configured to log necessary information needed to gain greated visibility into environment.

* CMK Auditing
  - Enable `CloudTrail` logging in AWS Account -> KMS API calls are logged in defined S3 bucket. Contain following info: _Source IP Address, request author, request timestamp etc._
  - Monitor CloudTrail logs (using aws services or other security tool) for specific **actions**: `ScheduleKeyDeletion, PutKeyPolicy, DeleteAlias, DisableKey, DeleteImportedKeyMaterial`
  - KMS emits `CloudWatch` **event** when key is: **rotated, deleted, imported key material expires**

* CMK Validation
  - Use `AWS Config` to make sure AWS services are set up properly e.g. EBS volumes should be encrypted -> Use `ENCRYPTED_VOLUMES` AWS Config rule.
  - Correlate Tags. Tags can be used to verify that correct CMK is being used for given action e.g. _CMK in use belongs to same business category as the resource it's being used on_

## Infrastructure Security

## Data protection

## Incident response
  * Security automation - use **lambda** to disable CMK instead of human intervention. In case of incident response action **cut off can be achieved in minutes** by using automation.
  * Delete or disable CMKs:
    - disabled keys prevent to be used when no longer needed, can be **enabled** again. Disabled keys are still stored in AWS so **charges remain**. More expensive solution than delete.
    - deleted keys **cannot be restored again**. Decision whether to delete should be made carefully.
    - **deletion period** - to make sure CMKs are not deleted by accident/mistake AWS KMS enforces a minimum waiting period of **7 days** to delete keys. Max deletion period for keys is **30 days**.
