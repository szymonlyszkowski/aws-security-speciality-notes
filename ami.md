# Creating secure AMIs
[How to share AMIs publically in secure way](https://aws.amazon.com/articles/how-to-share-and-use-public-amis-in-a-secure-manner/)

* Delete whole **shell history** (may contain access keys or other private data)
* Put **private keys & x509 certs** in a location which is not bundled e.g. instance store
* Remove **authorized_keys**: `find / -name "authorized_keys" –exec rm –f {} \;`
* Remove credentials to 3rd party applications (if using)
* Prevent any preconfigured remote logging -> delete the existing syslog config and restart the syslog service.
  ```
    rm /etc/syslog.conf
    service rsyslog restart
  ```
