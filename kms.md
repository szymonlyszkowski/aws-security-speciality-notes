## CMKs
* Can be imported only **with the same** key material
* If you want a different key material you need to create new CMK & provide same alias to not update application configuration
* CMKs can be rotated manually using CLI or AWS Console


## AWS Managed keys
* Rotated by default automatically
* Rotation of managed keys **cannot** be disabled
* Default rotation period is **3** years

### Key Material:
When to **reimport** _key material_:
* Key has *expired*
* Key was *lost* (by accident)
* Key was *deleted* (by accident)



TODO:

1. AWS Owned keys
2. Data key
3. Envelope encryption
4. ABAC (attribute based access control) vs. aliases
5. Key material
6. Generation of key pair
7. KeyId
8. Grant
9. Auditing of KMS key usage -> CloudTrail
10. Key Spec
11. Symmetric vs. assymetric keys
12. Custom Key Stores -> HSM
13. Grant (temp access)
