# AWS Architecting

## AWS Cloud Best Practices – Design Principles

-> Scalability => vertical & horizontal 

-> Disposable Resources => servers should be disposable & easily configured

-> Automation => Serverless, Infrastructure as a Service, Auto Scaling...

-> Loose Coupling

-> Services, not Servers => Use managed services, databases, serverless, ...

## Well Architected Framework 6 Pillars

-> they are not something to balance, or trade-offs, they’re a synergy

### Operational Excellence

-> includes the ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures

Design Principles: 

* Perform operations as code
* Make frequent, small, reversible changes
* Refine operations procedures frequently
* Anticipate failure 
* Learn from all operational failures
* Use managed services
* Implement observability for actionable insights

### Security

-> includes the ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies

Design Principles:
* Implement a strong identity foundation
* Enable traceability
* Apply security at all layers
* Automate security best practices 
* Protect data in transit and at rest
* Keep people away from data
* Prepare for security events
* Shared Responsibility Model

### Reliability

-> ability of a system to recover from infrastructure or service disruptions, dynamically acquire computing resources to meet demand, and mitigate disruptions such as misconfigurations or transient network issues

Design Principles:
* Test recovery procedures
* Automatically recover from failure
* Scale horizontally to increase aggregate system availability
* Stop guessing capacity
* Manage change in automation

### Performance Efficiency

-> includes the ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve

Design Principles:
* Democratize advanced technologies
* Go global in minutes
* Use serverless architectures
* Experiment more often
* Mechanical sympathy

### Cost Optimization

-> includes the ability to run systems to deliver business value at the lowest price point

Design Principles:
* Adopt a consumption mode
* Measure overall efficiency
* Stop spending money on data center operations
* Analyze and attribute expenditure
* Use managed and application level services to reduce cost of ownership

### Sustainability

-> the sustainability pillar focuses on minimizing the environmental impacts of running cloud workloads 

Design Principles:
* Understand your impact
* Establish sustainability goals
* Maximize utilization
* Anticipate and adopt new, more efficient hardware and software offerings
* Use managed services
* Reduce the downstream impact of your cloud workloads

## AWS Well-Architected Tool

-> free tool to review your architectures against the 6 pillars Well-Architected Framework and adopt architectural best practices

## AWS Customer Carbon Footprint Tool

-> track, measure, review, and forecast the Carbon emissions generated from your AWS usage

## AWS Cloud Adoption Framework (AWS CAF)

-> helps you build and then execute a comprehensive plan for your digital transformation through innovative use of AWS

### CAF Perspectives and Foundational Capabilities Business Capabilities

* Business Perspective => helps ensure that your cloud investments accelerate your digital transformation ambitions and business outcomes
* People Perspective => serves as a bridge between technology and business, accelerating the cloud journey to help organizations more rapidly evolve to a culture of continuous growth, learning, and where change becomes business-as-normal, with focus on culture, organizational structure, leadership, and workforce
* Governance Perspective => helps you orchestrate your cloud initiatives while maximizing organizational benefits and minimizing transformation-related risks

### CAF Perspectives and Foundational Capabilities Business Capabilities

* Platform Perspective => helps you build an enterprise-grade, scalable, hybrid cloud platform; modernize existing workloads; and implement new cloud-native solutions

* Security Perspective => helps you achieve the confidentiality, integrity, and availability of your data and cloud workloads

* Operations Perspective => helps ensure that your cloud services are delivered at a level that meets the needs of your business. 

### AWS CAF – Transformation Domains

* Technology => using the cloud to migrate and modernize legacy infrastructure, applications, data and analytics platforms...
* Process => digitizing, automating, and optimizing your business operations
* Organization => Reimagining your operating model 
* Product => reimagining your business model by creating new value propositions (products & services) and revenue models

### AWS CAF – Transformation Phases

* Envision => demonstrate how the Cloud will accelerate business outcomes by identifying transformation opportunities and create a foundation for your digital transformation
* Align => identify capability gaps across the 6 AWS CAF Perspectives which results in an Action Plan
* Launch => build and deliver pilot initiatives in production and demonstrate incremental business value
* Scale => expand pilot initiatives to the desired scale while realizing the desired business benefits


## AWS Right Sizing

-> cloud is elastic

-> right sizing is the process of matching instance types and sizes to your workload performance and capacity requirements at the lowest possible cost

-> scaling up is easy so always start small

It’s important to Right Size:
* before a Cloud Migration
* continuously after the cloud onboarding process (requirements change over time)

# AWS Ecosystem

DEVELOPER:
* Business hours email access to Cloud Support Associates
* General guidance: < 24 business hours
* System impaired: < 12 business hours

BUSINESS:
* 24x7 phone, email, and chat access to Cloud Support Engineers
* Production system impaired: < 4 hours
* Production system down: < 1 hour

ENTERPRISE:
* Access to a Technical Account Manager (TAM)
* Concierge Support Team (for billing and account best practices)
* Business-critical system down: < 15 minutes

## AWS Marketplace

-> digital catalog with thousands of software listings from 
independent software vendors

## AWS Professional Services & Partner Network

-> the AWS Professional Services organization is a global team of experts

APN (AWS Partner Network):
* APN Technology Partners
* APN Consulting Partners
* APN Training Partners
* AWS Competency Program
* AWS Navigate Program

## AWS IQ

-> quickly find professional help for your AWS projects

## AWS re:Post

-> AWS-managed Q&A service offering crowd-sourced, expert-reviewed answers to your technical questions about AWS that replaces the original AWS Forums

-> questions from AWS Premium Support customers that do not receive a response from the community are passed on to AWS Support engineers

### Knowledge Center

-> contains the most frequent & common questions and requests

## AWS Managed Services (AMS)

-> provides infrastructure and application support on AWS

-> AMS offers a team of AWS experts who manage and operate your infrastructure for security, reliability, and  availability