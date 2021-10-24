### EC2 Instance recovery

A recovered instance is identical to the original instance, including:
* instance ID
* private IP addresses
* Elastic IP addresses
* instance metadata

**recovery action** can be added to CW when ` StatusCheckFailed_System` appears
More details can be found [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UsingAlarmActions.html#AddingRecoverActions) & [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-recover.html)
