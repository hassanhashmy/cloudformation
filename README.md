# Cloudformation
These are Re-Usable-Multiapplication-CloudFormation-Templates


# The Challenge
These Templates are in yaml language and have generic format. These template helps us to deploy 3 kind of different environments
- Production
- UAT
- Test

You can define what environment you wanted to build and it will use that word in all files as prefix. These templates are launching different AWS resources such as
- EC2
- S3
- VPC
- WAF
- CloudFront
- Security Groups
- NACL
- Nat Gateways
- Internet Gateways
- Virtual Private Gateways
- Route Table
- Autoscalling Groups
- Elastic Loadbalancer
- IAM Roles
- Rout53
- Web ACL Lambda
- RDS
- Launch Configurations
- CodeDeploy
- Elastic Redis
- Elastic Search

These resources are being mapped with other resources automatically by importing their values.
