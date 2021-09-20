# Active Directory service

### Additional layer of security on user level

* Enable MFA on logging to AWS Managed Active Directory service
* Active Directory **password policies** e.g. Lock account after specified number of failed logins


### Encryption in transit
* Use **LDAPS** (LDAP over SSL)
  * [Client side LDAPS](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/ms_ad_ldap_client_side.html)
  * [Server-side LDAPS](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/ms_ad_ldap_server_side.html)
