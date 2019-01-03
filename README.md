# AWS CLI Useful Commands
Here I add useful commnads to the list.

## Getting The Latest AMI:
### Ubuntu 16.04
```bash
aws ec2 describe-images --region ap-southeast-2 --filters Name=name,Values=ubuntu/images/hvm-ssd/ubuntu-xenial-16.04-amd64*  --query 'Images[*].[ImageId,CreationDate]' --output text  | sort -k2 -r  | head -n1 | cut -f1
```
