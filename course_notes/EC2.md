# Elastic Compute Cloud (EC2)

-> Infrastructure as a Service

It mainly consists in the capability of :
* Renting virtual machines (EC2)
* Storing data on virtual drives (EBS)
* Distributing load across machines (ELB)
* Scaling the services using an auto-scaling group (ASG)

Configuration options:
* Operating System (OS): Linux, Windows or Mac OS
* How much compute power & cores (CPU) 
* How much random-access memory (RAM)
* How much storage space: 
    * Network-attached (EBS & EFS)
    * hardware (EC2 Instance Store)
* Network card: speed of the card, Public IP address
* Firewall rules: security group
* Bootstrap script (configure at first launch): EC2 User Data 

## EC2 User Data

-> bootstrapping = launching commands when a machine starts (only run once at the instance first start)

-> EC2 user data is used to automate boot tasks such as:

* Installing updates
* Installing software
* Downloading common files from the internet

-> The EC2 User Data Script runs with the root user

## EC2 Instance Types

-> you can use different types of EC2 instances that are optimised for different use cases (https://aws.amazon.com/ec2/instance-types/)

-> great for a diversity of workloads such as web servers or code repositories

### Compute Optimized

Great for compute-intensive tasks that require high performance processors:
* Batch processing workloads
* Media transcoding
* High performance web servers
* High performance computing (HPC)
* Scientific modeling & machine learning
* Dedicated gaming servers

### Memory Optimized

-> fast performance for workloads that process large data sets in memory

Use cases: 
* High performance, relational/non-relational databases
* Distributed web scale cache stores
* In-memory databases optimized for BI (business intelligence)
* Applications performing real-time processing of big unstructured data

### Storage Optimized

-> great for storage-intensive tasks that require high, sequential read and write access to large data sets on local storage

Use cases: 
* High frequency online transaction processing (OLTP) systems
* Relational & NoSQL databases
* Cache for in-memory databases (for example, Redis)
* Data warehousing applications
* Distributed file systems

## Security Groups

-> fundamental for security network in AWS (control how traffic is allowed into or out of our EC2 Instances) => firewall for EC2

-> only contains allow rules (reference by IP or Security Groups)

-> can be attached to multiple instances

They regulate:

* Access to Ports
* Authorised IP ranges – IPv4 and IPv6
* Control of inbound network
* Control of outbound network

![security_groups](..\materials\images\security_groups.png)

Classic Ports to know: 

* 22 = SSH (Secure Shell) - log into a Linux instance
* 21 = FTP (File Transfer Protocol) – upload files into a file share
* 22 = SFTP (Secure File Transfer Protocol) – upload files using SSH
* 80 = HTTP – access unsecured websites
* 443 = HTTPS – access secured websites
* 3389 = RDP (Remote Desktop Protocol) – log into a Windows instance

## SSH

-> it allows you to control a remote machine, all using the command line

-> you can use EC2 Connect Instance as well

## EC2 Instances Purchasing Options

* On demand: coming and staying in resort whenever we like, we pay the full price
* Reserved: like planning ahead and if we plan to stay for a long time, we may get a good discount.
* Savings Plans: pay a certain amount per hour for certain period and stay in any room type (e.g., King, Suite, Sea View, ...)
* Spot instances: the hotel allows people to bid for the empty rooms and the highest bidder keeps the rooms. You can get kicked out at any time
* Dedicated Hosts: We book an entire building of the resort
* Capacity Reservations: you book a room for a period with full price even you don’t stay in it

![ec2_prices](..\materials\images\ec2_prices.png)

## Shared Responsibility Model for EC2

AWS:

* Infrastructure (global network security)
* Isolation on physical hosts
* Replacing faulty hardware
* Compliance validation

User:

* Security Groups rules
* Operating-system patches and updates
* Software and utilities installed on the EC2 instance
* IAM Roles assigned to EC2 & IAM user access management
* Data security on your instance








