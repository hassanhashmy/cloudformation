# Cloudformation
These are Re-Usable-Multiapplication-CloudFormation-Templates


# The Challenge

Need an implementation on AWS which will be track by SCM and implement all changes, updated or new provisioning of Infrastructure with CD/CI using repository and without accessing servers directly. For this challenge we need to design templates in a manner so that we can make different branches and build same code. As there are 3 environment which we required to provision.
- Production
- UAT
- Test

Infrastructure code must be remain same and Infrastructure naming convention must be user friendly and easy to manageable by using 1 account or 2 accounts doesn't mater. Templates should work in all environments and it must have some parameters and dynamic values which can be change or may vary.
We were given 2 AWS accounts in our case 1 for totally Production in which some highly sensitive data like Credit Card, Home address, phone numbers, emails will be processed, and the other 1 should be for UAT and Test. But we have to design templates like all environments are in same account so we have to differentiate them.
Which means we have to design re-usable templates.

Infrastructure Design must have these features:

- Highly Available
- Fault Tolerant
- Cost Efficient
- Well Architected
- Performance Optimized
- Highly Secure
- Auto Provisionable
- Auto Configurable

Template Design must have these features:

- Re-usable
- Code Remain same from test to production
- Must work with CD/CI
- Must Fulfill DevOps Flow


# Solution

These Templates are in YAML language and have generic format. These template helps us to deploy 3 or more, kind of different environments
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

# Note
These templates required some minor changes so please read the template that how these are written and then start implementation. Basic help is mention below.

# Basic Help
- Choose the region and define in template. This is design for Sydney region
- This template is design for 12 different applications which makes 1 single platform so edit it as per your requirement. 
- First Create 2 s3 buckets by using folder number 1 as per your required name and upload all templates to 1st bucket. Leave blank other bucket for application code
- Then run IAM-Role-FlowLogs.yaml from Standalone folder
- Run VPC master
- Run Rout53 master
- Run Security Group master
- Run all master one by one
- Run remaining Standalone templates
