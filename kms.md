## CMKs
* Can be imported only **with the same** key material
* If you want a different key material you need to create new CMK & provide same alias to not update application configuration
* CMKs can be rotated manually using CLI or AWS Console


## AWS Managed keys
* Rotated by default automatically
* Rotation of managed keys **cannot** be disabled
* Default rotation period is **3** years
