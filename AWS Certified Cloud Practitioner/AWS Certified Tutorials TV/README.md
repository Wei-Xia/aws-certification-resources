## Lesson 1: What is cloud computing

### Why Cloud Computing

- Pay As You Use
- Lower TCO
- Reliability, Scalability, Sustainability
- Secure Storage
- Lower Capital Expenditure
- Frees Up Internal Resources
- Highly Auotomated
- Utility Based
- Easy & Agile Deployment
- Device & Location Independent
- 24x7 Support


### Advcantages of AWS Cloud Computing

- Variable Expenses
- Economies of Scale
- Stop Guessing
- Increase Speed and Agility
- Save Money
- Go Global

### Types of Cloud Computing

- Enterprise IT (legact IT)
- Infrastructure (as a Service)
- Platform (as a Service)
- Softwaer (as a Service)

### AWS Global Infrastructure

- Regions
- Availability Zones (AZ)

## Lesson 2: AWS Computing

### Elastic Cloud Compute (EC2)

- Elastic Computing
- Completely Controlled
- Flexible
- Integrated
- Reliable
- Secure
- Inexpensive

### Elastic Beanstalk

- Create Application
- Upload Version
- Launch Environment
- Manage Environment

### Lambda

- Upload your code to AWS Lambda
- Set up your code to trigger from other AWS services, HTTP endpoints, or in-app activity
- Lambda runs your code only when triggered, using only the computer resources needed
- Pay just for the compute time you use

## Lesson 3: A look into the AWS Console

An overview of AWS Console, not critial.

## Lesson 4: Creating a Billing Alarm

By using AWS CloudWatch, you can set up alarms for your billing exceeds certain amount of charge.

## Lesson 5: Launching an EC2 Instance

### Create an EC2 Instance

- Choose AMI
- Choose Instance Type
- Configure Instance
- Add Storage
- Add Tags
- Configure Security Group
- Review

### Purchase Options

- On demand
- Reserved
- Spot (bid)

## Lesson 6: S3 Buckets

### Storage Options

- Simple Storage Service (S3)
- Elastic Block Storage (EBS)
- Elastic File System (EFS)
- Glacier
- Storage Gateway

### Simple Storage Service (S3)

- Simple
- Durable (99.999999999%) - 11x9s 
- Scalable
- Secure
- Availbale
- Low Cost
- Integrated

### S3 Storage Classes

- S3 Standard
- S3 Intelligent Tiering
- S3 Standard Infrequent Access
- S3 One Zone Infrequent Access
- S3 Glacier
- S3 Glacier Deep Archive

### S3 Comparison

|                                    |  S3 Standard  | S3 Intelligent-Tiering* |  S3 Standard-IA  | S3 One Zone-IA†  |       S3 Glacier        | S3 Glacier Deep Archive |
| :--------------------------------: | :-----------: | :---------------------: | :--------------: | :--------------: | :---------------------: | :---------------------: |
|      Designed for durability       | 99.999999999% |      99.999999999%      |  99.999999999%   |  99.999999999%   |      99.999999999%      |      99.999999999%      |
|                                    |   (11 9’s)    |        (11 9’s)         |     (11 9’s)     |     (11 9’s)     |        (11 9’s)         |        (11 9’s)         |
|     Designed for availability      |    99.99%     |         99.90%          |      99.90%      |      99.50%      |         99.99%          |         99.99%          |
|          Availability SLA          |    99.90%     |           99%           |       99%        |       99%        |         99.90%          |         99.90%          |
|         Availability Zones         |      ≥3       |           ≥3            |        ≥3        |        1         |           ≥3            |           ≥3            |
| Minimum capacity charge per object |      N/A      |           N/A           |      128KB       |      128KB       |          40KB           |          40KB           |
|  Minimum storage duration charge   |      N/A      |         30 days         |     30 days      |     30 days      |         90 days         |        180 days         |
|           Retrieval fee            |      N/A      |           N/A           | per GB retrieved | per GB retrieved |    per GB retrieved     |    per GB retrieved     |
|         First byte latency         | milliseconds  |       millseconds       |   milliseconds   |   milliseconds   | select minutes or hours |      select hours       |
|            Storage type            |    Object     |         Object          |      Object      |      Object      |         Object          |         Object          |
|       Lifecycle transitions        |      Yes      |           Yes           |       Yes        |       Yes        |           Yes           |           Yes           |



## Lesson 7: Creating an S3 Bucket

### Create Bucket

- Name and region
- Configure options
- Set permissions
  - Private by default
- Review 

##Lesson 8: Elastic Block Storage

### Elastic Block Storage (EBS)

- High Performance Volumes
- Availability
- Encryption
- Access Management
- Snapshots

### EBS Volume Types

- Provisioned IOPS SSD (io1)
- General Purpose SSD (gp2)
- Throughput Optimized HDD (st1)
- Cold HDD (sc1)

### EBS Volume Types Comparison

|                                | Solid State Drives (SSD)                                     |                                                              | Hard Disk Drives (HDD)                                       |                                                              |
| ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Volume Type                    | EBS Provisioned IOPS SSD (io1)                               | EBS General Purpose SSD (gp2)*                               | Throughput Optimized HDD (st1)                               | Cold HDD (sc1)                                               |
| Short Description              | Highest performance SSD volume designed for latency-sensitive transactional workloads | General Purpose SSD volume that balances price performance for a wide variety of transactional workloads | Low cost HDD volume designed for frequently accessed, throughput intensive workloads | Lowest cost HDD volume designed for less frequently accessed workloads |
| Use Cases                      | I/O-intensive NoSQL and relational databases                 | Boot volumes, low-latency interactive apps, dev & test       | Big data, data warehouses, log processing                    | Colder data requiring fewer scans per day                    |
| API Name                       | io1                                                          | gp2                                                          | st1                                                          | sc1                                                          |
| Volume Size                    | 4 GB - 16 TB                                                 | 1 GB - 16 TB                                                 | 500 GB - 16 TB                                               | 500 GB - 16 TB                                               |
| Max IOPS**/Volume              | 64,000                                                       | 16,000                                                       | 500                                                          | 250                                                          |
| Max Throughput***/Volume       | 1,000 MB/s                                                   | 250 MB/s                                                     | 500 MB/s                                                     | 250 MB/s                                                     |
| Max IOPS/Instance              | 80,000                                                       | 80,000                                                       | 80,000                                                       | 80,000                                                       |
| Max Throughput/Instance        | 1,750 MB/s                                                   | 1,750 MB/s                                                   | 1,750 MB/s                                                   | 1,750 MB/s                                                   |
| Price                          | $0.125/GB-month, $0.065/provisioned IOPS                     | $0.10/GB-month                                               | $0.045/GB-month                                              | $0.025/GB-month                                              |
| Dominant Performance Attribute | IOPS                                                         | IOPS                                                         | MB/s                                                         | MB/s                                                         |

### EBS Features

- Data Lifecycle Manager
- Elastic Volumes
- Snapshots
- Optimized Instances
- Availability & Durability
- Encryption

## Lesson 9: Create an Elastic Block Storage Volume

An overview of EBS in AWS Console, not critial.

## Lesson 10: Elastic File Storage

### Elastic File System (EFS)

- Dynamic Elasticity
- Scalable
- Fully Managed
- Cost Effective
- Shared File Storage

### EFS, S3, EBS Comparsion

|                 |                                | File - Amazon EFS                                            | Object - Amazon S3                                           | Block - Amazon EBS                                           |
| --------------- | ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Performance     | Per-operation latency          | Low, consistent                                              | Low, for mixed request types, and integration with CloudFront | Lowest, consistent                                           |
|                 | Throughput scale               | Multiple GBs per second                                      | Multiple GBs per second                                      | Single GB per second                                         |
| Characteristics | Data Availability / Durability | Stored redundantly across multiple AZs                       | Stored redundantly across multiple AZs                       | Stored redundantly in a single AZ                            |
|                 | Access                         | One to thousands of EC2 instances or on-premises servers, from multiple AZs concurrently | One to millions of connections over the web                  | Single EC2 instance in a single AZ                           |
|                 | Use Cases                      | Web serving and content management, enterprise applications, media and entertainment, home directories, database backups, develop tools, container storage, big data analytics | Web serving and content management, media and entertainment, backups, big data analytics, data lake | Boot volumes, transactional and NOSQL databases, data warehousing and ETL |

## Lesson 11: Identity Access Management

Using IAM, you can create user identities ("IAM users") and assign custom permissions sets ("IAM policies") to those users.

### Identity Access Management (IAM) benefits

- Shared Access
- Granular Permissions
- Integrated
- Multi-Factor Authentication (MFA)
- Identify Fedration
- Secure Access
- Compliance

### Accessing IAM

- Management Console
- HTTPS API
- CLI
- SDKs

### How it works

1. Principle
2. Request
3. Authentication
4. Authorization
5. Actions/Operations
6. Resources

### Best Practices

- Lock away root user access keys
- Create individual IAM Users
- Use groups to assign permissions
- Use AWS defined policies
- Grant least privilege
- Review IAM permission regularly
- Strong password policy
- Multi-Factor Authenticatios for privilege users
- Use roles for EC2 applications
- Use roles to delegate permissions
- Don't share access keys
- Rotate credentials
- Remove unnecessary credentials
- Use policy conditions
- Monitor activity

## Lesson 12: Creating Users and Groups

### Types

- Groups
- Users
- Roles
- Policies
- Identity providers

## Lesson 13: Relational Database Service

### Database Options

- PostgreSQL
- MySQL
- MariaDB
- Oracle
- Microsoft SQL Server
- Amazon Aurora

### Relational Database Service (RDS) benefits

- Easy to administer
- Scalable
- Available and Durable
- Fast
- Secure
- Inexpensive

### PostgreSQL

- Rich features and extensions

- Reliability and compliance

- Open source license

- History

- Popular uses

 ### MySQL

- High availability read replicas
- Easy managed deployments
- Fast, predictable storage
- Backup and recovery
- Monitoring and Metrics

  ###MariaDB

- Easy managed deployments
- High performance and availability 
- Low and flexible prcing
- Easy to scale
- Simplified security

## Lesson 14: Launching a MySQL Database instance

An demonstration on creating MySQL Database from AWS RDS

## Lesson 15: Aurora Database

### Aurora Benefits

- High Performance
- Low Cost
- Secure
- MySQL & Postgre SQL
- Scalable
- Availability and Durability
- Fully Managed

## Lesson 16: Amazon CloudFront

### What is CloudFront

Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly enviroment.

### CloudFront Benefits

- Fast and Global
- Security
- Highly Pergrammable
- Deep Integration

### CloudFront Features

- Security
- Availability
- Performance
- DevOps Friendly
- Lambda Edge

## Lesson 17: Creating a CloudFront Distribution

An demonstration on creating a CloudFront instance

## Lesson 18: Route 53

### Route 53 Benefits

- Highly Available
- Flexible
- Secure & Scalable
- Simple & Fast
- Deep Integration

### Key Features

- Resolver
- Traffic Flow
- Latency based routing
- Geo & Private DNS
- DNS Failover
- Health Checks
- Domain Registration
- Elastic Load Balancing Integration

## Lesson 19: Elastic Load Balancing

### Elastic Load Balancing Benefits

- High Availability
- Elastic
- Robutst & Hybrid
- Secure
- Flexible

### Key Features

- Application Load Balancer: Application Load Balancer is best suited for load balancing of HTTP and HTTPS traffic and provides advanced request routing targeted at the delivery of modern application architectures.
- Network Load Balancer: Network Load Balancer is best suited for load balancing of TCP traffic where extreme performance is required.
- Classic Load Balancer: Classic Load Balancer provides basic load balancing across multiple Amazon EC2 instances and operates at both the request level and connection level.

## Lesson 20: Virtual Private Cloud

Amazon Virtual Private Cloud (Amazon VPC) lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.

You have complete control over your virtual networking environment, including selection of your own IP address range, creation of subnets, and configuration of route tables and network gateways.

### VPC Features

- Secure
- Simple
- Scalable

### VPC Benefits

- Direct Internet connection
- Network Address Translation (NAT)
- Secure datacenter connection
- Multiple VPC Connection
- Private connection without NAT
- AWS PrivateLink

### VPC Limitations

- 5 VPCs per account
- 4 secondary IP ranges
- 200 subnets
- 5 Elastic IP addresses
- 10 Hardware VPN connections

## Lesson 21: Creating a Virtual Private Cloud

An demonstration on creating a VPC instance.

## Lesson 22: Migration

### Options Available

- Application Discovery Service
- Database Migration Service
- Server Migration Service
- Snowball

### Application Discovery Service Benefits

- Reliable
- Engage with experts
- Encryption
- Integration
- Process flow
  - Discover
  - Identify
  - Measure
  - Explore

### Database Migration Service Benefits

- Simple
- Reliable
- Low cost
- Range of support

### Snowball and Snowmobile

- High speed
- Scalable
- Tamper resistant
- Low cost

## Lesson 23: Management Tools

### AWS Management Tools

- CloudWatch
- Trusted Advisor
- CloudTrail
- EC2 System Manager
- AWS Config
- CloudFormation

### CloudFormation

1. Code your infrastructure from scratch with the CloudFormation template language, in either YAML or JSON format, or start from many available sample templates.
2. Check out your template code locally, or upload it into an S3 bucket.
3. Use AWS CloudFormation via the browser console, command line tools or APIs to create a stack based on your template code.
4. AWS CloudFormation provisions and configures the stacks and resources you specified on your template.

### CloudWatch

1. **Collect**: Metrics and logs from all your AWS resources, applications, and services that run on AWS and on-premises servers
2. **Monitor**: Visualize applications and infrastructure with CloudWatch dashboards; correlate logs and metrics side by side to troubleshoot and set alerts with CloudWatch Alarms.
3. **Act**: Automate response to operational changes with CloudWatch Events and Auto Scaling.
4. **Analyze**: Up to 1-second metrics, extended data retention, and real-time analysis with CloudWatch Metrics Math.

### CloudTrail

1. **Capture**: Record activity in AWS services as AWS CloudTrail events
2. **Store**: AWS CloudTrail delivers events to the AWS CloudTrail console, Amazon S3 buckets, and optionally Amazon CloudWatch Logs.
3. **Act**: Use Amazon CloudWatch Alarms and Events to take action when important events are detected.
4. **Review**: View recent events in the AWS CloudTrail console, or analyze log files with Amazon Athena.

### EC2 System Manager

1. **Group Resources**: Create groups of resources across different AWS services, such as applications or different layers of an application stack.
2. **Visualize Data**: View aggregated operational data by resource group.
3. **Take Action**: Respond to insights and automate operational actions across resource groups.

### EC2 Manager Tools

- Run Command
- State Manager
- Inventory
- Maintenance Window
- Patch Manager
- Automation

### AWS Config

AWS Config automatically evaluates the recorded configurations against the configurations you specify:

- AWS Config & APIs & Console
- Amazon SNS
- Amazon CloudWatch
- Amazon S3

### AWS Trusted Advisor

- Cost Optimization
- Performance
- Security
- Fault Tolerance
- Service limits

### AWS Personal Health Dashboard

- Service Health
- Proactive Notifications
- Troubleshooting Guidance
- Integration & Automation

## Lesson 24: Messaging Tools

### A suite of Tools

- Simple Queue Service (SQS)
- Simple Notification Service (SNS)
- Simple Email Service (SES)

### Simple Queue Service (SQS)

- Benefits
  - Eliminate Admin Overhead
  - Keep sensitive data secure
  - Reliably deliver message
  - Scale Elastically
- Features
  - Standard and FIFO Queues
  - Robust functionality
  - Use with other AWS Service

### Simple Notification Service (SNS)

Fully-managed pub/sub messaging and event-driven computing service

- SNS Topic
- Message Filtering & Fanout

