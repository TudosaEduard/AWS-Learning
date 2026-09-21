# AWS Organization

-> allows to manage multiple AWS accounts

-> main account => master account

Cost Benefits:

* consolidated billing across all accounts
* pricing benefits from aggregated usage
* pooling of Reserved EC2 instances for optimal savings

-> API is available to automate AWS account creation

-> restrict account privileges using Service Control Policies

Consolidated Billing:

* Combined Usage – combine the usage across all AWS accounts in the AWS Organization to share the volume pricing, Reserved Instances and Savings Plans discounts
* One Bill – get one bill for all AWS Accounts in the AWS Organization

## Multi Account Strategies

-> create accounts per department, per cost center, per dev / test / prod, based on regulatory restrictions(using SCP), for better resource isolation (ex: VPC), to have separate per-account service limits, isolated account for logging

-> use tagging standards for billing purposes

-> enable CloudTrail on all accounts

## Service Control Policies (SCP)

-> whitelist or blacklist IAM actions

-> does not apply to the Master Account

-> is applied to all the Users and Roles of the Account (does not affect service-linked roles)

-> must have an explicit Allow

## AWS Control Tower

-> easy way to set up and govern a secure and compliant multi-account AWS environment based on best practices

-> runs on top of AWS Organizations

## AWS Resource Access Manager (AWS RAM)

-> share AWS resources that you own with other AWS accounts (with any account or within your Organization)

-> avoid resource duplication

## AWS Service Catalog

-> quick self-service portal to launch a set of authorized products pre-defined by admins

# Pricing Models in AWS

AWS has 4 pricing models:

* Pay as you go: pay for what you use, remain agile, responsive, meet scale demands
* Save when you reserve: minimize risks, predictably manage budgets, comply with long-terms requirements
* Pay less by using more: volume-based discounts
* Pay less as AWS grows

-> with a new AWS account, you get up to $200 in credits

You choose between:

* Free Plan => expires in 6 months or when credits are consumed
* Paid Plan => charged after you consume your credits
* Both Plans => have access to Always Free Services

## Compute Pricing – EC2

* On-demand instances: 
    * Minimum of 60s
    * Pay per second (Linux/Windows) or per hour (other)
* Reserved instances:
    * Up to 75% discount compared to On-demand on hourly rate
    * 1 or 3 years commitment
    * All upfront, partial upfront, no upfront
* Spot instances:
    * Up to 90% discount compared to On-demand on hourly rate
    * Bid for unused capacity
* Dedicated Host:
    * On-demand
    * Reservation for 1 year or 3 years commitment
* Savings plans as an alternative to save on sustained usage

## Compute Pricing – Lambda & ECS

* Lambda:
    * Pay per call
    * Pay per duration
* ECS:
    * EC2 Launch Type Model: No additional fees, you pay for AWS resources stored and created in your application
* Fargate:
    * Fargate Launch Type Model: Pay for vCPU and memory resources allocated to your applications in your containers

## Storage Pricing – S3

Storage class: 
* S3 Standard
* S3 Infrequent Access
* S3 One-Zone IA
* S3 Intelligent Tiering
* S3 Glacier
* S3 Glacier Deep Archive

## Database Pricing - RDS

Database characteristics: 
* Engine
* Size
* Memory class

Purchase type:
* On-demand
* Reserved instances (1 or 3 years) with optional up-front

## Content Delivery – CloudFront

* Pricing is different across different geographic regions
* Aggregated for each edge location, then applied to your bill

## Networking Costs in AWS per GB

* Use Private IP instead of Public IP for good savings and better network performance
* Use same AZ for maximum savings (at the cost of high availability)

# Savings Plan

-> commit a certain $ amount per hour for 1 or 3 years 

-> easiest way to setup long-term commitments on AWS

-> EC2 Savings Plan, Compute Savings Plan, Machine Learning Savings Plan (66% for EC2, Fargate or Lambda)

# AWS Compute Optimizer

-> reduce costs and improve performance by recommending optimal AWS resources for your workloads

-> uses Machine Learning to analyze your resources’ configurations and their utilization CloudWatch metrics

# Billing and Costing Tools

* Estimating costs in the cloud:
    * Pricing Calculator => estimate the cost for your solution architecture
* Tracking costs in the cloud:
    * Billing Dashboard => Billing and Cost Management Dashboard
    * Cost Allocation Tags => use cost allocation tags to track your AWS costs on a detailed level (AWS generated tags / User-defined tags)
    * Cost and Usage Reports => contains the most comprehensive set of AWS cost and usage data available, including additional metadata about AWS services, pricing, and reservations (e.g., Amazon EC2 Reserved Instances (RIs))
    * Cost Explorer => visualize, understand, and manage your AWS costs and usage over time (forecast usage up to 12 months based on previous usage)
* Monitoring against costs plans:
    * Billing Alarms => billing data metric is stored in CloudWatch us-east-1
    * Budgets => create budget and send alarms when costs exceeds the budget (4 types of budgets: Usage, Cost, Reservation, Savings Plans)

# AWS Cost Anomaly Detection

-> continuously monitor your cost and usage using ML to detect unusual spends

-> sends you the anomaly detection report with root-cause analysis

# AWS Service Quotas

-> notify you when you’re close to a service quota value threshold

-> create CloudWatch Alarms on the Service Quotas console

# Trusted Advisor

Analyze your AWS accounts and provides recommendation on 6 categories:

* Cost optimization
* Performance
* Security
* Fault tolerance
* Service limits
* Operational Excellence

# AWS Support Plans Pricing

AWS Basic Support Plan:

* Customer Service & Communities - 24x7 access to customer service, documentation, whitepapers, and support forums.
* AWS Trusted Advisor
* AWS Personal Health Dashboard

AWS Developer Support Plan:

* Business hours email access to Cloud Support Associates
* Unlimited cases / unlimited contacts

AWS Business Support Plan (24/7):

* Used if you have production workloads
* Trusted Advisor  – Full set of checks + API access
* 24x7 phone, email, and chat access to Cloud Support Engineers

AWS Enterprise On-Ramp Support Plan (24/7):

* Used if you have production or business critical workloads
* Access to a pool of Technical Account Managers (TAM)  
* Concierge Support Team (for billing and account best practices)
* Infrastructure Event Management, Well-Architected & Operations Reviews

AWS Enterprise Support Plan (24/7):

* Used if you have mission critical workloads
* Access to AWS Incident Detection and Response 
* Business-critical system down response under 15 minutes