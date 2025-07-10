Identity Centre => IAM

IAM - Password Policy (You can setUp this)
Set a minium password length
Require specific character types
Allow all IAM users to change their own passwords
Password Expiration

MFA => Multi Factor Authentication

Universal 2nd Factor (U2F) Security Key
Hardware Key Fob MFA

IAM => ACCOUNT SETTINGS => PASSWORD POLICY

Access to AWS => 
AWS Management Console (protected by password + MFA)
AWS Command Line Interface (CLI): protected by access keys
AWS Software Developer Kit (SDK): Protected by access keys

Access keys are generated through the AWS Console
Users manage their own access keys (Never share Access Keys)

SDK => JS, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++
Mobile SDKs (Android, iOS)
IoT Device SDK's (Embedded C, Arduino) 

AWS CLI is built on AWS SDK for Python (boto)

USER => USER => Security Credentials (Create Access Keys)

IAM Roles => Some AWS Services will need to perform actions on your behalf
TO do so , we will assign permissions to AWS services with IAM Roles

Example: if an EC2 instance wants to use any AWS service or create a new instance we need to make sure to assign ROLE to EC2 instance to enable it to function as expected


IAM Security Tools
IAM Credentials Report (account-level)
A report that lists all your account's users and the status of their various credentials

IAM Access Advisor (user-level)
Access advisor shows the service permissions granted to a user and when those services were last accessed.
You can use this information to revise your policies

IAM => ACCESS REPORT => CREDENTIAL REPORT 

Access Advisor named Last Access (Users => click on the user => right most on the table)

Shared Responsibility Model for IAM

AWS
Infrastructure (global network security)
Configuration and vulnerability analysis
Compliance Validation

User
User Groups, Roles, Policies management and monitoring
Enable MFA on all accounts
Rotate all your keys often
Use IAM tools to apply appropriate permissions
Analyze access patterns and review permissions


Generally one cannot access Billing information other than root account even if one has administrator access. To actually see the billing info we need to make sure to enable IAM user and role access to Billing information from the root account

EC2 is one of the most popular of AWS' offering
EC2 = Elastic Compute Cloud = Infrastructure as a Service 

Rent Vm's EC2
Storing data on virtual drives EBS
Distributing load across machines ELB
Scaling the services using an Auto Scaling Group (ASG )