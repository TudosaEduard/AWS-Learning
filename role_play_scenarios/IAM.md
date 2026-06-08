# Communicating IAM and Security Best Practices to Non-Technical Stakeholders

## Scenario

You are a Cloud Practitioner at a mid-sized retail company that recently started migrating its operations to AWS. The company's leadership has raised concerns about securely managing access to their AWS resources. In a meeting with one of the managers, you are tasked to explain the concepts of IAM, such as users, groups, and roles, and share how policies, MFA, and other tools help mitigate risks. You also need to outline the company's part in the Shared Responsibility Model for cloud security.

## Goals

1. Explain the concepts of IAM, including users, groups, and roles, in a clear and non-technical manner.

    AWS uses a service called IAM, which stands for Identity and Access Management. In simple terms, IAM helps us control who can access AWS, what they can access, and what actions they can perform.

    There are three important IAM concepts: users, groups, and roles.

    An IAM user represents one person or one application that needs access to AWS. An IAM group is a way to manage permissions for multiple people at once. An IAM role is different from a user. A role is temporary access that can be given to a person, application, or AWS service when needed. For example, an application can use a role to read files from storage without storing a permanent username and password.

2. Provide clear examples of how IAM policies, MFA, and AWS security tools can prevent credential misuse and mitigate risks.

    Access is controlled using IAM policies. A policy is basically a rule that says what is allowed or denied. This follows the principle of least privilege, which means people and systems should only receive the access they need to do their job.

    To reduce the risk of stolen passwords, we should also use MFA, or multi-factor authentication. This means that even if someone’s password is stolen, the attacker still needs a second verification method, such as a code from an authentication app.

    WS also provides tools that help reduce security risks such as IAM Credentials Report -> a report that lists all your account's users and the status of their various credentials or IAM Access Advisor -> shows the service permissions granted to a user and when those services were last accessed. 

3. Communicate the principles of the AWS Shared Responsibility Model relating to securing access.

    This connects to the AWS Shared Responsibility Model. AWS is responsible for security of the cloud, which means protecting the physical data centers, hardware, networking, and core infrastructure. Our company is responsible for security in the cloud, which means managing users, permissions, passwords, MFA, data access, and service configurations.

4. Address Mike’s concerns and ensure he has a better understanding of how to implement access management best practices.

    So, Mike, AWS provides the secure foundation and the security tools, but we must use them correctly. That means we should avoid sharing accounts, give each person their own access, use groups for teams, use roles for applications and temporary access, apply least privilege, turn on MFA, and regularly review permissions.