# AWS KMS

## KMS & IAM
  * IAM Policies usage within KMS
  * Key Policies
  * Cross account sharing keys
  * Encryption context
  * MFA for keys

## Detective controls

## Infrastructure Security

## Data protection

## Incident response
  * Security automation - use **lambda** to disable CMK instead of human intervention. In case of incident response action **cut off can be achieved in minutes** by using automation.
  * Delete or disable CMKs:
    - disabled keys prevent to be used when no longer needed, can be **enabled** again. Disabled keys are still stored in AWS so **charges remain**. More expensive solution than delete.
    - deleted keys **cannot be restored again**. Decision whether to delete should be made carefully.
    - **deletion period** - to make sure CMKs are not deleted by accident/mistake AWS KMS enforces a minimum waiting period of **7 days** to delete keys. Max deletion period for keys is **30 days**.
