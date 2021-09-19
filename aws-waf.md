# AWS WAF


## Deployment to Production

### Operational Readiness
* Select date & time when you have **lowest** traffic
* Prepare runbooks for security teams (TODO add what runbook should contain)
* If using AWS Shield **Advanced** you can use AWS DDoS response team (DRT).  The DRT helps you analyze the
suspicious activity and assists you in mitigating the issue
### Deployment
* Use **count mode** to catch any potential false positives that were not in STG.
* Don't mix AWS WAF with other WAF offerings for evaluation as this can result in **conflicts in how rules are matched**
TODO Post Deployment

## Cost considerations
* AWS WAF **standalone** pricing - per used webACL rules & amount of request inspected
* When using AWS Shield **Advanced** - no charges for using AWS WAF & AWS Firewall Manager (just pay for charges AWS Shield Advances). **Useful especially when using workloads with high volume requests.**  
