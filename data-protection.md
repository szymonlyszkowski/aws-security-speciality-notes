## Data Classification
* Identify the data within your workload
* Define data protection controls
* Define data lifecycle management
* Automaton of idenification and protection

## Data at rest

* Tokenization - a way to present a data in a different state(otherwise sensitive piece of information). Token must be **meaningless** & **must not** be derived from data it is tokenizing.
* Encryption - transforming content in a manner makes it unreadabe without necessary secret key.

* Secure Key management
* Enforce encryption at rest
* Enforce access control
* Auditing of encryption keys usage
* Keep people away from data
* Automate data at rest protection:
  - AWS Config Rules (validation all EBS are encrypted, remediate noncompliant resources)
  - AWS Security Hub (verify number of different controls using automated checks)
