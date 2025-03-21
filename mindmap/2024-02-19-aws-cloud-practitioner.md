---
layout:     mindmap
title:      AWS Cloud Practitioner Review Cheat Sheet
date:       2024-01-13 15:26:00
summary:    AWS Elastic Block Store Mindmap
categories:  
permalink:  /aws-cloud-practitioner-review
---


## AWS Cloud Advantages

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 1
---

- **Trade fixed expense for variable expense**
Pay only when you consume
- **Benefit from massive economies of scale**
Lower pay-as-you-go prices
- **Stop guessing capacity**
Scale up & down as required (Elastic)
- **Increase speed & agility**
Experiment fast 
- **Stop spending money maintaining data centers**
Avoid undifferentiated heavy lifting
- **Go global in minutes**
Multiple Regions around the world

</script>
</div>


## AWS Compute Options

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---

- **EC2**: Virtual Machines in the Cloud
- **EC2 Auto Scaling**: Add/Remove EC2 instances based on load
Monitor & replace unhealthy instances (Auto Scaling Group)
- **Elastic Load Balancing**: Load balance between multiple EC2 instances
- **AWS Elastic Beanstalk**: Simplified Deployment of EC2 instances (with ELB)
Fast Provision & Deployment of Python or Java or NodeJs or .. apps
- **Amazon ECS**: AWS Specific Container Orchestration
- **AWS Fargate**: Serverless ECS
- **Amazon EKS**: Kubernetes based Container Orchestration
- **AWS Lambda**: Serverless Compute (Pay for invocations)
Only for short duration workloads
- **AWS Batch**: Run batch applications on AWS

</script>
</div>

## EC2 Pricing Options

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---

- **Spot Instances($)**: Lowest cost
Interruptible, short-term cost-sensitive workloads
- **Reserved Instances($$)**: Reserve EC2 instances 
1 year or 3 year commitment
- **Savings Plans($$$)**: 1 year or 3 years commitment 
Flexibility: EC2 or AWS Fargate or Lambda
- **On-Demand($$$$)**: Flexible, for immediate workloads
Always running for ONLY 1 week or 3 months
- **Dedicated Hosts($$$$$)**: Your own dedicated server
Useful for specific licensing & security needs
</script>
</div>

## AWS Storage Options

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **Elastic Block Store (EBS)**: Network Block Storage
More durable. Attach & Detach as needed.
- **Instance Store**: Ephemeral Attached Block Storage
Lifecycle tied to EC2 instance
- **Elastic File Store (EFS)**: Scalable file storage
For Linux-based applications, supports NFS protocol
- **Amazon FSx for Windows File Server**: Managed Windows-based file storage
Supports SMB protocols
- **Amazon S3**: Serverless Object Storage
Flexible: Standard (Frequently accessed data), Glacier (Archive data)
Intelligent-Tiering (unknown access patterns)
Supports Versioning: Prevent Accidental Deletion
Create Low Latency Static Website with Amazon CloudFront
- **AWS Storage Gateway**: Hybrid Storage (on-premise + cloud)
AWS Storage File Gateway (Hybrid file share)
AWS Storage Tape Gateway (Tape backups)
AWS Storage Volume Gateway (Hybrid block storage)

</script>
</div>

## AWS Database & Caching Options

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---

- **Amazon RDS**: Managed Relational OLTP Databases 
MySQL, SQL Server, Oracle, DB2, MariaDB, PostgreSQL
- **Amazon Aurora**: Global Relational Database with Serverless Option
MySQL, PostGreSQL compatible
- **Amazon DynamoDB**: Serverless NoSQL/Non Relational database
Single-digit millisecond responses for million of TPS
- **Amazon Neptune**: Graph Database
Store & navigate data with complex relationships
- **Amazon Redshift**: Relational OLAP Database (Datawarehouse)
Petabyte scale with a serverless option (Reduced Management)
- **Amazon ElastiCache**: In memory database/cache
Option 1: Redis(persistent - leader boards)
Option 2: Memcached (non-persistent - pure cache)
</script>
</div>


## Networking & Content Delivery in AWS

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---

- **Amazon VPC**: Virtual Network to secure resources
- **Subnet**: Separate private & public resources
- **Internet Gateway**: Allows Public Subnets to accept traffic to/from internet
- **NAT Gateway**: Allow internet traffic from private subnets
- **Security Group**: Control traffic at an instance level
- **NACL**: Control traffic at Subnet level
- **VPC Peering**: Connect one VPC with other VPCs
- **VPC Flow Logs**: Enable logs to debug problems
Monitor traffic In & Out of VPC
- **AWS Direct Connect**: Dedicated, fast, private connection to on-prem
- **AWS VPN**: Encrypted tunnel over internet to on-premises
- **Amazon Route 53**: Highly Available Global DNS service
- **Amazon CloudFront**: Distribute content from edge locations
Users get lower latency (ex: S3 static website)
- **Global Accelerator**: Static IP routes to closest endpoint (EC2, ELB,..)
Faster connections for global users (Edge locations)
</script>
</div>

## Authentication, Authorization & Encryption in AWS

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS IAM**: Control Access to AWS resources 
Who can access AWS resources (authentication)
What can they do (authorization)
- **IAM users**: Users created in an AWS account
- **IAM groups**: Collection of IAM users
- **IAM roles**: Temporary identities without credentials
- **IAM policies**: Define permissions
Attach with IAM users, IAM groups & IAM roles
- **Amazon Cognito**: Web/Mobile App User Auth. & Authorization
Supports SAML & Social Media Logins
- **AWS KMS**: Create keys & encrypt your data
Integration with Storage, Database & other AWS services


</script>
</div>

## IAM Best Practices


<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---

- **Users** – Create individual users
- **Groups** – Manage permissions with groups
- **Permissions** – Grant least privilege
- **Auditing** – Turn on AWS CloudTrail
- **Password** – Configure a strong password policy
- **MFA** – Enable MFA for privileged users
- **Roles** – Use IAM roles for Amazon EC2 instances
- **Sharing** – Use IAM roles to share access
- **Rotate** – Rotate security credentials regularly
- **Root** – Reduce or remove use of root

</script>
</div>



## DevOps in AWS
<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **Versioning and Source Control**: AWS CodeCommit (Git)
- **CI/CD orchestration**: AWS CodePipeline
  - **Build and Test Code**: AWS CodeBuild
  - **Automate Deployment**: AWS CodeDeploy
- **Observability - Tracing**: X-Ray
- **Observability - Metrics & Alarms**: CloudWatch
- **Observability - Logging**: CloudWatch
- **IaC - AWS CloudFormation**: YAML/JSON based scripts
Stack Set: Provision same resources in multiple regions
- **IaC - AWS CDK**: IaC in your favorite programming language
- **IaC - AWS SAM**: Easy provisioning & deployment of Serverless apps
- **App Configuration - Secrets**: Secret Manager
Flexible **Auto Rotation** + Costlier + **Integration with RDS, ..** +
- **App Configuration - App Config + Secrets**: Parameter Store
Secrets + Configuration + **Cost Effective**


</script>
</div>

## Playing with AWS

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS CLI**: Interact with AWS services from command line
Write scripts to automate as needed
Best for: Users comfortable with CLI
- **AWS CloudShell**: Browser-based command line interface
No need to configure software on your machine
Best for: Users who want to use command line from the browser
- **AWS Management Console**: Web-based GUI 
Access & manage AWS resources
Best for: Users that prefer a GUI to interact with AWS
- **AWS SDK**: Call AWS services from your code
Libraries available for various programming languages
Best for: Integrate AWS services into their apps
- **IaC**: AWS CloudFormation, AWS CDK, AWS SAM
</script>
</div>

## Loose Coupling in AWS
<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **Amazon SQS**: Push, Pull Messaging
Decoupling microservices for scalability
- **Amazon SNS**: Publish subscribe pattern
Bulk notifications & Mobile push support (Email + SMS)
- **Amazon EventBridge**: Build event-driven architectures
React to events generated from AWS services, SaaS & custom apps
EventBridge Scheduler provides scheduling services
- **Amazon Kinesis**: Real-time data streaming & analytics
Process & analyze streaming data (for example, from IOT device) at scale
- **Amazon MSK**: Managed Service for Apache Kafka
Fully managed, highly available Kafka service
- **AWS Step Functions**: Workflow service to automate processes
Orchestrate serverless workflows with visual drag-and-drop interface
- **Amazon Simple Email Service (Amazon SES)**: Managed email service
High deliverability & scalable email service
</script>
</div>


## Analytics & Intelligence in AWS

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **Amazon Redshift**: Relational OLAP Database (Datawarehouse)
Petabyte scale with a serverless option (Reduced Management)
- **Amazon EMR (Elastic MapReduce)**: Big data framework service
Big data using Spark, Hadoop
- **AWS Glue**: Discover, prepare, and integrate data at any scale
Serverless data preparation & load service (ETL)
- **Amazon Athena**: Run serverless SQL on Amazon S3 data
Ad-hoc data querying without server setup
- **Amazon QuickSight**: Visualization
Business Intelligence Dashboards for insights
NLP powered by machine learning for easier analysis
- **Amazon Elasticsearch Service (Amazon ES)**: Search & analytics engine
Real-time application monitoring & log analysis
</script>
</div>

## Machine Learning in AWS
<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **Build Simple Models**: Amazon SageMaker Auto ML
Without needing data scientists
Needs Limited/no-code experience
- **Build Complex Models**: Amazon SageMaker
Needs data scientists & team
- **Pre-Built Models**
  - **Amazon Comprehend**: Analyze Unstructured Text
  - **Amazon Rekognition**: Search & Analyze Images & Videos
  - **Amazon Transcribe**: Powerful Speech Recognition
  - **Amazon Polly**: Turn Text into Lifelike Speech
  - **Amazon Translate**: Powerful Neural Machine Translation
  - **Amazon Personalize**: Add real-time recommendations to your apps
  - **Amazon Forecast**: Time-series forecasting service
  - **Amazon Lex**: Build Voice & Text Chatbots
  - **Amazon Bedrock**: Access Generative AI Foundation Models
</script>
</div>

## Simplifying Governance in AWS

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS Artifact**: Get access to AWS security & compliance reports
- **AWS Service Catalog**: Create & govern curated IaC templates
- **AWS Market Place**: Deploy Third Party Applications Quickly
- **AWS Trusted Advisor**: Get recommendations from AWS
Cost optimization, Performance, Security
Fault tolerance (resiliency), Service limits, Operational Excellence
Checks SG rules allowing unrestricted access - 0.0.0.0/0
- **Amazon CloudTrail**: Audit AWS Service calls
Track all activity on AWS services
Ex: Track EC2 instance start/stop events
Ex: Monitor EBS volume creation/deletion
Ex: Monitor security group modifications
Ex: Monitor bucket creation/deletion

</script>
</div>

## Managing Multiple AWS Accounts

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS Organizations**: Centralized mgmt for multiple AWS Accounts
Create separate AWS accounts for different business units
Create separate AWS accounts for different environments
- **Consolidated Billing**: Get one bill across multiple accounts
Feature of AWS Organizations
Get discounts at enterprise level
- **AWS IAM Identity Center**: Manage IAM for multiple AWS Accounts
Centrally create & connect your workforce identities
Streamline single sign-on access on AWS
- **AWS Firewall Manager**: Manage Firewalls across multiple AWS Accounts
Supports Security Groups, WAF, Shield, ..
Automatically enforce your defined security policies

</script>
</div>


## Managing Costs in AWS

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS Billing & Cost Management**: Centralized dashboard
Manage your payment methods, Pay your bills
- **Pricing Calculator**: Estimate cost of AWS resources
- **AWS Budgets**: Set a Budget
Get alerts from CloudWatch when you exceed the budget
- **AWS Cost Explorer**: Visualize your AWS costs
Get Right Sizing Recommendations
Filter by Region, AZ, tags etc
See future cost projection
- **AWS Compute Optimizer**: Resource optimization recommendations
RightSizing for EC2, ECS, Lambda, EBS
- **Free to use** but pay for resources provisioned
AWS Management Console, AWS CloudFormation, AWS Organizations,...
FREE: AWS Cost Explorer (UI), Identity & Access Management (IAM), ...

</script>
</div>

## Improving Your Security Posture in AWS

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS Security Hub**: Cloud security posture mgmt (CSPM) service
Automate security best practice checks
Aggregate security alerts into a single place 
Understand overall security posture across multiple AWS accounts
- **AWS WAF**: Block SQL Injection + XSS
Protect your web applications from OWASP Top 10 exploits
Can be deployed on CloudFront, ALB, API Gateway, ..
- **AWS Inspector**: Automated vulnerability mgmt
Discover software vulnerabilities & unintended network exposure
Discovers & scans EC2 instances, container images, & Lambda fns
- **Amazon Macie**: Detect PII in S3
Recognize & classify sensitive data
- **AWS Shield**: Always-on DDoS protection
Integrates with Route 53, CloudFront, EC2, ELB..
</script>
</div>


## AWS Well-Architected Framework - Pillars

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 1
---

- **Operational excellence**: Ability to support development
Run workloads effectively
Gain insight into operations and continuously improve
- **Security**: Ability to protect data, systems, & assets 
- **Reliability**: Ability of a workload to perform its intended function
Correctly and Consistently
- **Performance efficiency**: Ability to use computing resources efficiently
Maintain that efficiency as demand changes and technologies evolve
- **Cost optimization**: Ability to run systems at the lowest price point
- **Sustainability**: Meet needs without impacting future generations
</script>
</div>


## AWS Well-Architected Framework - Design Principles

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 1
---

- **Operational excellence**: Use managed services
Perform operations as code
Frequent, small, reversible changes
Anticipate & learn from failure
- **Security**: Apply security at all layers
Protect data in transit & at rest
Maintain traceability
- **Reliability**: Automatically recover from failure
Scale horizontally, Stop guessing capacity
Manage change with automation
- **Performance efficiency**: Go global in minutes
Experiment more often, Use serverless architectures
- **Cost optimization**: Implement Cloud Financial Management
Analyze & attribute expenditure
- **Sustainability**: Understand your impact, Establish goals
Maximize utilization, Reduce the downstream impact
</script>
</div>

## AWS CAF (Cloud Adoption Framework)

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS CAF**: Framework to guide your cloud adoption
- **Envision phase**: Identify & prioritize opportunities
Define success metrics and desired outcomes
- **Align phase**: Identify capability gaps
Address gaps through upskilling, ...
- **Launch phase**: Deliver pilot initiatives
Execute pilot projects
Iterate and learn from initial deployments
- **Scale phase**: Expand & deliver business value
Expand successful pilots
Continuously optimize your cloud environment
</script>
</div>

## AWS CAF Perspectives

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **Business**: Ensure that your cloud investments accelerates:
your digital transformation ambitions and business outcomes
- **People**: Bridge between technology and business
Evolve to a culture of continuous growth, learning
Change becomes business-as-normal
- **Governance**: Orchestrate your cloud initiatives 
Goal: Maximizing organizational benefits
Goal: Minimizing transformation-related risks
- **Platform**: Build an enterprise-grade cloud platform
Modernize existing workloads
Implement cloud-native solutions
- **Security**: Achieve CIA for data and workloads
Confidentiality, Integrity and Availability
- **Operations**: Deliver cloud services that meet business needs
</script>
</div>


## AWS CAF Capabilities

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 1
---

- **Business**: Strategy Mgmt, Product Mgmt, Portfolio Mgmt
  Innovation Mgmt, Data Monetization, Strategic Partnership
- **People**: Organizational Alignment, Organization Design
  Culture Evolution, Cloud Fluency
- **Governance**: Program & Project Mgmt, Cloud Financial Mgmt, 
Application Portfolio Mgmt, Risk Mgmt, Data Curation, Data Governance
- **Platform**: Architecture, Provisioning & Orchestration
Modern Appln Development, Data Engineering, Data Architecture, CI/CD
- **Security (CIA)**: Identity & Access Mgmt, Infrastructure Protection
Vulnerability Mgmt, Incident Response, Application Security
Threat Detection, Data Protection, Security Assurance
- **Operations**: Event Mgmt (AIOps), Incident & Problem Mgmt
Configuration Mgmt, Application Mgmt, Patch Mgmt, 
Availability & Continuity Mgmt, Observability, Change & Release Mgmt
</script>
</div>

## Managing Your AWS Migration

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---

- **AWS Migration Hub**: Streamlines Migration Oversight
Central hub for tracking migration progress
- **Application Discovery Service**: During initial analysis and planning
Collect on-premise infrastructure data
- **AWS Migration Evaluator**: Focus on financial and technical feasibility
Understand the implications, costs, and technical considerations of migration
Identify the right AWS services and configurations (right-sizing) for your needs
- **Database Migration Service (DMS)**: Seamless Database Transition
Ensures minimal downtime for critical database workloads
- **Snowmobile**: Securely transfers petabytes and exabytes of data 
Recommended for >10 Petabytes
- **Snowball Edge**: Enhanced Data Transfer & Edge Computing
Offers offline data transfer & local computing capabilities
Suitable for remote or disconnected environments
- **AWS DataSync**: Accelerated Online Data Transfer
Automates data synchronization tasks

</script>
</div>


## Getting Help From AWS


<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS Knowledge Center**: Articles & videos with FAQs
Based on requests that AWS receives from customers
- **AWS Professional Services**: Get help from AWS specialists
Plan, migrate, & manage your AWS journey
- **AWS Partner Network**: Get help from 3rd-party Certified Consultants
Migrate Workloads With Professional Guidance
- **AWS Managed Services**: Ongoing mgmt. of your AWS infra.
Extend your team with operational support from AWS 
Get help for monitoring, patch, backup, & cost optimization
- **AWS Support Plans**: Get support from AWS
**Basic (FREE)**: AWS Trusted Advisor Basic + AWS Health + Docs
**Developer(PAID)**: Business hours email support
**Business(PAID)**: 24/7 phone, web, & chat support
**Enterprise(PAID)**: Lots of additional features:
AWS Managed Services(PAID) + TAM for proactive guidance +
Consultative reviews & guidance based on your apps
</script>
</div>


## Few Important Terminologies

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **Agility**: Play, experiment, try new things, launch quickly
A big advantage of the cloud!
- **Availability**: Ensure applications is available as much as possible
Multiple Instances, Multi AZ, Multi Region
- **Disaster Recovery**: Plan to recover from outages 
Minimize downtime & data loss
EC2 - Have Copies of AMI in Different Regions, EBS - Take Snapshots
- **Durability**: Ensure you do NOT lose data
Multiple Copies, Multi AZ, Multi Region
- **Economies of Scale**: Advantages of managing millions of servers
AWS is expected to pass the cost benefits to end users
- **Elasticity**: Scale resources up or down quickly based on demand
- **RightSizing**: Choose the optimal resources for your workload
AWS: AWS Compute Optimizer, AWS Cost Explorer
- **Threat Detection**: Detect threats ahead of time
AWS: Amazon GuardDuty 

</script>
</div>

## Exploring Key AWS Reports

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **IAM Credential Report**: Auditing & Compliance
List all your AWS IAM users
List status of credentials - MFA & last use of access keys
- **IAM Access Analyzer**: Identifies resources shared with an external entity
Example: S3 bucket that can be accessed by the public
IAM Role that can be accessed by another AWS account
- **Access Analyzer for S3**: Analyze access to S3
Identify S3 buckets configured to allow public access
- **S3 Inventory Report**: Manage your storage
List of the objects in the source bucket & metadata for each object
- **AWS Cost & Usage Report**: Understand your AWS expenses
Analyze AWS spending & usage trends
- **AWS Trusted Advisor**: Recommendations for your AWS account
**Categories**: Cost optimization, Performance, Security
Fault tolerance, Service limits, Operational Excellence
</script>
</div>

## Understanding AWS Global Infrastructure

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **Region**: A physical location offering various AWS services
Deploy global highly-available, low-latency applications
Adhere to government regulations
- **Availability Zone**: Isolated, & physically separate Zones with a region
High availability within the same region
- **Edge Locations**: Faster Delivery Hubs for Your Cloud Data
Deliver static content faster (CloudFront)
Route traffic through closest edge location (Global Accelerator)
Access S3 objects faster (Amazon S3 Transfer Acceleration)
- **AWS Outposts**: Mini-AWS you set up in your own data center
You manage the hardware, AWS manages the software
AWS like experience with complete control
- **AWS Local Zones**: Extension of the AWS cloud 
Brought closer to a specific city or region
Fully Managed by AWS
Faster access for users in a specific location (think online gaming, live streaming)
- **AWS Wavelength**: Use communications service providers 5G networks
Build applications that deliver ultra-low latencies to mobile devices
</script>
</div>

## Shared Responsibility Examples

<div class="markmap">
<script type="text/template">
---
markmap:
  colorFreezeLevel: 2
---
- **AWS**: Security of the Cloud
Physical security of data centers
Hardware and network infrastructure
Virtualization layer (HostOS)
- **Customer**: Security in the Cloud
Data Security (Encrypting data - rest & transit)
Proper Configuration (IAM, Security Groups, ..)
- **Example 1**: Amazon EC2 (IaaS)
**AWS:** Physical security, hardware, network infra., virtualization (HostOS)
**Customer:** Guest OS, Appl. Software, Security Group config, Data,..
- **Example 2**: Amazon S3 (PaaS)
**AWS:** Infrastructure, OS, networking, durability, availability
**Customer:** Data & configuration - Encryption, IAM, ACLs, Lifecycle,..
- **Example 3**: Amazon RDS (PaaS)
**AWS:** Infrastructure, OS, networking, DB software installation, patching
**Customer:** Data & configuration - Backup, Encryption, IAM, ..
</script>
</div>

&nbsp;&nbsp;&nbsp;