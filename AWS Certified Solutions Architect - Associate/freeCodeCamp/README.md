# Table of Contents

- [Simple Storage Service (S3)](#simple-storage-service--s3-)
  - [Introduction to S3](#introduction-to-s3)
    - [Object Storage](#object-storage)
    - [S3 Object](#s3-object)
    - [S3 Bucket](#s3-bucket)
  - [S3 - Storage Classes](#s3---storage-classes)
    - [Standard (default)](#standard--default-)
    - [Intelligent Tiering](#intelligent-tiering)
    - [Standard Infrequently Accessed (IA)](#standard-infrequently-accessed--ia-)
    - [One Zone IA](#one-zone-ia)
    - [Glacier](#glacier)
    - [Glacier Deep Archive](#glacier-deep-archive)
  - [S3 - Storage Classes Comparison](#s3---storage-classes-comparison)
  - [S3 - Security](#s3---security)
  - [S3 - Encryption](#s3---encryption)
    - [Encryption In Transit](#encryption-in-transit)
    - [Server Side Encryption (SSE) - Encryption At Rest](#server-side-encryption--sse----encryption-at-rest)
    - [Client-Side Encryption](#client-side-encryption)
  - [S3 - Data Consistency](#s3---data-consistency)
    - [New Objects (PUTS)](#new-objects--puts-)
    - [Overwrite (PUTS) or Delete Objects (DELETES)](#overwrite--puts--or-delete-objects--deletes-)
  - [S3 - Cross Region Replication](#s3---cross-region-replication)

---

# Simple Storage Service (S3)

## Introduction to S3

- Object-based storage service
- Serverless storage in the cloud

### Object Storage

data storage architecture that manages data as objects, as opposed to other storage architectures:

- **file system** which manages data as a file and fire hierarchy
- **block storage** which manages data as blocks within sectors and tracks

S3 provides you with **unlimited storage**. You don't need to think about the underlying infrastructure.

The S3 console provides an interface for you to upload and access your data.

### S3 Object

Object contain your data. They are like files.

Object may consist of:

- **Key**: this is the name of the object
- **Value**: the data itself made up of a sequence of bytes
- **Version ID**: when versioning enabled, the version of object
- **Metadata**: additional information attached to the object

You can store data from **_0 Bytes_** to 5 Terabytes in size

### S3 Bucket

Buckets hold objects. Buckets can also have folders which in turn hold objects.

S3 is a universal namespace so bucket names must be unique (just like a domain name).

## S3 - Storage Classes

Trade **Retrieval Time**, **Accessibility** and **Durability** for **Cheaper Storage**.

From top to bottom is the most expensive to the cheapest.

### Standard (default)

Fast! 99.99% Availability, 11 9's Durability. Replicated across at least three AZs.

### Intelligent Tiering

Uses ML to analyze your object usage and determine and appropriate storage class. Data is moved to the most cost-effective access tier, without any performance impact or added overhead.

### Standard Infrequently Accessed (IA)

Still fast! Cheaper if you access files less than once a month. Additional retrieval fee is applied. 50% less than Standard (reduced availability)

### One Zone IA

Still fast! Objects only exist in one AZ. Availability is 99.5%, but cheaper than Standard IA by 20% less because of reduce durability. Data could get destroyed. A retrieval fee is applied.

### Glacier

For long-term cold storage. Retrieval of data can take minutes to hours but the off is very cheap storage.

### Glacier Deep Archive

The lowest cost storage class. Data retrieval time is 12 hours.

## S3 - Storage Classes Comparison

S3 Guarantees:

- Platform is built for 99.99% availability
- Amazon guarantee 99.9% availability
- Amazon guarantees 11' 9s of durability

|                                  | Standard | Intelligent Tiering | Standard IA | One-zone IA |    Glacier    | Glacier Deep Archive |
| :------------------------------: | :------: | :-----------------: | :---------: | :---------: | :-----------: | :------------------: |
|            Durability            |  11 9's  |       11 9's        |   11 9's    |   11 9's    |    11 9's     |        11 9's        |
|           Availability           |  99.99%  |        99.9%        |    99.9%    |    99.5%    |      N/A      |         N/A          |
|         Availability SLA         |  99.99%  |         99%         |     99%     |     99%     |      N/A      |         N/A          |
|               AZs                |    >3    |         >3          |     >3      |      1      |      >3       |          >3          |
| Min Capacity charger per storage |   N/A    |         N/A         |    128kb    |    128kb    |     40kb      |         40kb         |
|   Min storage duration charge    |   N/A    |       30 days       |   30 days   |   30 days   |    90 days    |       180 days       |
|          Retrieval fee           |   N/A    |         N/A         |   Per GB    |   Per GB    |    Per GB     |        Per GB        |
|        First byte latency        |    ms    |         ms          |     ms      |     ms      | mins to hours |        hours         |

## S3 - Security

All new buckets are PRIVATE when created by default.

Access control is configured using **Bucket Policies** and **Access Control Lists (ACL)**:

- **Access Control Lists**: Legacy feature of controlling access to buckets and objects.
- **Bucket Policies**: Use a policy to define complex rule access.

## S3 - Encryption

### Encryption In Transit

Traffic between your local host and S3 is achieved via **SSL/TLS**.

### Server Side Encryption (SSE) - Encryption At Rest

Amazon help you encrypt the object data.

S3 Managed Key (Amazon manages all the keys):

- **SSE-AES**: S3 handles the key, uses AES-256 algorithm
- **SSE-KMS**: Envelope encryption, AWS KMS and you manage the keys
- **SSE-C**: Customer provided key (you manage the keys)

### Client-Side Encryption

You encrypt your own files before uploading them to S3.

## S3 - Data Consistency

### New Objects (PUTS)

**Read After Write Consistency:**

When you upload a new S3 object, you are able read immediately after writing.

### Overwrite (PUTS) or Delete Objects (DELETES)

**Eventual Consistency:**

When you overwrite or delete an object it takes time for S3 to replicate version to AZs.

If you were to read immediately, S3 may return you an old copy. You need to generally wait a few seconds before reading.

## S3 - Cross Region Replication (CRR )

When enabled, any object that is uploaded will be **automatically replicated** to another region(s), provides higher durability and potential disaster recovery for object.

You must have **versioning** turned on both the **source** and **destination** buckets. You can have cross-region replication replicate to another AWS account.

## S3 - Versioning

Versioning will:

- Store all versions of an object in S3
- Once enabled, it can NOT be disabled, only suspended on the bucket
- Fully integrated with S3 Lifecycle rules
- MFA Delete feature provides extra protection against deletion of your data

## S3 - Lifecycle Management

Lifecycle Management can:

- Automate the process of moving objects to different Storage classes or deleting objects all together.
- Be used together with **versioning**.
- Be applied to **current** and **previous** version.

Use-case:

1. Set to move object to Glacier after 7 days
2. Set to permanently delete after 365 days

## S3 - Transfer Acceleration

Fast and secure transfer of files **over long distances** between your end users and an S3 bucket.

Utilize **CloudFront**'s distributed **Edge Locations**.

Instead of uploading to your bucket, users use a **_distinct URL_** for an Edge Location.

As data arrives at the Edge Location, it will automatically routed to S3 over a specially optimized network plan (Amazon's backbone network).

## S3 - Presigned URLs

Generate a URL which provides you temporary access to an object to either upload or download object data. Presigned URLs are commonly used to provide access to **private object**.

You can use AWS CLI or AWS SDK to generate presigned URLs.

A sample presigned URL will look like this:

```
https://mybucket.s3.amazonaws.com/myobject?AWSAccessKeyId=AKJAXXXXXXXXX&Expires=1503608432743&Signature=fdjasfadshf3432%fds
```

It will include:

1. Access Key
2. Expired Timestamp
3. Signature

## S3 - MFA Delete

**MFA Delete** ensures users can not delete objects from a bucket unless they provide their MFA code.

MFA Delete can only be enabled under these conditions:

1. The **AWS CLI** must be used to turn on MFA
2. The bucket must have **versioning turned on**

Only the bucket owner logged in as **Root User** can **DELETE** objects from bucket.

## S3 - Cheat Sheet

- **Simple Storage Service** (S3) Object-based storage. Store **unlimited** amount of data without worry of underlying storage infrastructure
- S3 replicates data across at least 3 AZs to ensure 99.99% availability and 11' 9s of durability
- Objects contain your data (they're like files)
- Objects can be size anywhere from **0 Bytes** up to 5 Terabytes
- Buckets contain objects. Buckets can also contain folders which can in turn can contain objects
- When you upload a file to S3 successfully, you'll receive a HTTP 200 code
- **Lifecycle Management** Objects can be moved between storage classes or objects can be deleted automatically based on a schedule
- **Versioning** Objects are giving a Version ID. When new objects are uploaded the old objects are kept. You can access any object version. When you delete an object the previous object is restored. Once Versioning is turned on, it can not be turn off, only suspended.
- **MFA Delete** enforce DELETE operations to require MFA token in order to delete an object. Must have versioning turned on to use. Can only turn on MFA Delete from the AWS CLI. Root Account is only allowed to delete object
- All new buckets are **private by default**
- Logging can be turned to on a bucket to log to track operations performed on object
- **Access Control** is configured using **Bucket Policies** and **Access Control List (ACL)**
- **Bucket Policies** are JSON documents which let you write complex control access
- **ACLs** are the legacy method (not deprecated) where you grant access to objects and buckets with simple actions.
- **Security in Transit** - Uploading files is done over SSL
- **SSE** stands for Server Side Encryption. S3 has **3 options** for SSE
- **SSE-AES** - S3 handles the key, uses AES-256 algorithm
- **SSE-KMS** - Envelope encryption via AWS KMS and you manage the key
- **SSE-C** - Customer provided key (you manage the keys)
- **Client-Side Encryption** - You must encrypt your own files before uploading them to S3
- **Cross Region Replication (CRR)** allows you to replicate files across regions for greater durability. You must have versioning turned on in the source and destination bucket. You can have CRR replicate to bucket in another AWS account
- **Transfer Acceleration** provide faster and secure uploads from anywhere in the world. Data is uploaded via distinct url to an Edge Location. Data is then transported to your S3 bucket via AWS backbone network
- **Presigned Urls** is a url generated via the AWS CLI and SDK. It provides temporary access to write or download object data. Presigned Urls are commonly used to access private objects.
- S3 has **6 different** Storage Classes:
  - **Standard**: Fast! 99.99% Availability, 11 9's Durability. Replicated across at least three AZs.
  - **Intelligent Tiering**: Use ML to analyze your object usage and determine the appropriate storage class. Data is moved to the most cost-effective access tier, without any performance impact or added overhead.
  - **Standard Infrequently Accessed (IA)**: Still Fast! Cheaper if you access files less than once a month. Additional retrieval fee is applied. 50% less than Standard (reduced availability).
  - **One Zone IA**: Still fast! Objects only exist in one AZ. Availability is 99.5%, but cheaper than Standard IA by 20% less (Reduce durability). Data could get destroyed. A retrieval fee is applied.
  - **Glacier**: For long term cold storage. Retrieval of data can take minutes to hours but the off is very cheap storage.
  - **Glacier Deep Archive**: The lowest cost storage class. Data retrieval time is 12 hours.

# Snowball

## Introduction to Snowball

- **Low Cost**: It cost thousands of dollars to transfer 100 TB over high speed internet. Snowball can reduce that costs by **1/5th**
- **Speed**: It can take 100 TB over 100 days to transfer over high speed internet. Snowball can reduce that transfer time by **less than a week**
- Snowball come in two sizes:
  - **50 TB** (42 TB of usable space)
  - **80 TB** (72 TB of usable space)

### Snowball features and limitations

- E-lnk display (shipping information)
- Tamper and weather proof
- Data is encrypted end-to-end (256-bit encryption)
- Use Trusted Platform Module (TPM): a specialized chip on an endpoint device that stores RSA encryption keys specific to the host system for hardware authentication
- For security purposes, data transfer must be completed within **90 days** of the Snowball being prepared
- Snowball can **Import** and **Export** from S3

## Snowball Edge

Similar to Snowball but with more storage and with local processing

- **Petabyte-scale** data transfer service
- **Move data onto AWS** via physical briefcase computer
- **More storage** and on-site **computer capabilities**
- Snowball Edge come in two sizes:
  - **100 TB** (42 TB of usable space)
  - **100 TB Clustered** (45 TB per node)

### Snowball features and limitations

- LCD display (shipping information and other functionality)
- Can undertake local processing and edge-computing workloads
- Can use in a cluster in groups of 5 to 10 devices
- Three options for device configurations
  - storage optimized (24 vCPUs)
  - compute optimized (54 vCPUs)
  - GPU optimized (54 vCPUs)

## Snowmobile

a 45-foot long ruggedize shipping container, pulled by a semi-trailer truck.

Transfer up to 100 PB per Snowmobile.

AWS personnel will help you connect your network to the snowmobile and when data transfer is completed, they'll drive it back to AWS to import into S3 or Glacier.

### Security Features

- GPS Tracking
- Alarm monitoring
- 24/7 video surveillance
- an escort security vehicle while in transit (optional)

## Snowball - Cheat Sheet

- **Snowball** and **Snowball Edge** is a rugged container which contains a storage device
- **Snowmobile** is a 45-foot long ruggedize shipping container, pulled by a semi-trailer truck
- Snowball and Snowball Edge is for **peta-scale** migration. Snowmobile is for **exabyte-scale** migration
- **Low Cost** thousands of dollars to transfer 100 TB over high speed internet, Snowball is **1/5th**
- **Speed** 100 TB over 100 days to transfer over high speed internet, Snowball takes **less than a week**
- **Snowball come in two sizes**:
  - **50 TB** (42 TB of usable space)
  - **80 TB** (72 TB of usable space)
- **Snowball Edge come in two sizes**:
  - **100 TB** (42 TB of usable space)
  - **100 TB Clustered** (45 TB per node)
- **Snowmobile comes in one size**: 100 PB
- You can both **export** and **import** data using Snowball or Snowmobile
- You can import into **S3** or **S3 Glacier**
- **Snowball Edge** can undertake local processing and edge-computing workloads
- **Snowball Edge** can use in a cluster in groups of 5 to 10 devices
- **Snowball Edge** provides three options for device configurations
  - storage optimized (24 vCPUs)
  - compute optimized (54 vCPUs)
  - GPU optimized (54 vCPUs)

# Virtual Private Cloud

## Core Components

Think of a AWS VPC as your own **personal data center**.

Give you complete control over your **virtual networking environment**.

![001](./assets/001.jpg)

Combining these components and services is what makes up your VPC:

- Internet Gateway (IGW)
- Virtual Private Gateway (VPN Gateway)
- Routing Tables
- Network Access Control Lists (NACLs) - Stateless
- Security Groups (SG) Stateful
- Public Subnets
- Private Subnets
- Nat Gateway
- Customer Gateway
- VPC Endpoints
- VPC Peering

## VPC Key Features

- VPCs are **Region Specific** they do not span regions
- You can create up to **5 VPC** per region
- Every region comes with a default VPC
- You can have **200 subnets** per VPC
- You can use **IPv4 CIDR Block** and in addition to a **IPv6 CIDR Block** (the address of the VPC)
- **Cost nothing**: VPC, Route Table, Nacls, Internet Gateways, Security Groups and Subnets, VPC Peering
- **Some things cost money**: eg. NAT Gateway, VPC Endpoints, VPC Gateway, Customer Gateway
- **DNS hostname**: Your instance have domain name addresses

## Default VPC

AWS has a default VPC in every region so you can **immediately** deploy instances.

- Create a VPC with a size with 16 IPv4 CIDR block (172.31.0.0/16)
- Create a size with 20 **default subnet in each Availability Zone**
- Create a **Internet Gateway** and connect it to your default VPC
- Create a **default security group** and associate it with your default VPC
- Create a **default network access control list (NACL)** and associate it with your default VPC
- Associate the **default DHCP (Dynamic Host Configuration Protocol)** options set for your AWS account with your default VPC
- When you create a VPC, it automatically has a main route table

## Default Everywhere IP

**0.0.0.0/0** is also known as default, it represents **all possible IP addresses**.

When we specify **0.0.0.0/0** in our route table for IGW, we are allowing internet access.

When we specific **0.0.0.0/0** in our security group inbound rules, we are allowing all traffic from the internet access our public resources.

When you see **0.0.0.0/0**, just think of giving access from anywhere or the internet.

## VPC Peering

**VPC Peering** allows you to connect one VPC with another over a **direct network route** using **private IP addresses**.

- Instances on peered VPCs behave just like they are on the **same network**
- Connect VPCs across **same** or **different AWS accounts** and **regions**
- Peering uses a **Star Configuration: 1 Central VPC - 4 other VPCs**
- **No Transitive Peering** (peering must take place directly between VPCs)
  - Needs a one to one connect to immediate VPC
- **No Overlapping CIDR Blocks**

## VPC Route Tables

Route tables are used to determine where **network traffic is directed**.

Each **subnet** in your VPC **must be associated** with a route table, a subnet can only be associated **with one route table at a time**, but you can associate multiple subnets with the same route table.

The Internet -> IGW -> Route -> Route Table -> Public subnet

## VPC Internet Gateway (IGW)

The Internet Gateway allows your VPC **access to the internet**.

IGW does **two** things:

- Provide a target in your VPC route tables for internet-routable traffic
- Perform network address translation (NAT) for instances that have been assigned **public IPv4 addresses**

To route out to the internet you need to add in your route tables you need to add a route.

To the internet gateway and set the Destination to be **0.0.0.0/0**.

## VPC Bastion / Jumpbox

![002](./assets/002.jpg)

Bastions are EC2 instances which are security harden. They are designed to help you gain access to your EC2 Instances via SSH or RCP. That are in a **private subnet**.

They are also known as Jump boxes because you are jumping from one box to access another.

NAT Gateways/Instances are only intended for EC2 instances to gain outbound access to the internet for things such as security updates.

NATs can't/shouldn't be used as Bastion.

## VPC Direct Connect

![003](./assets/003.jpg)

AWS Direct Connect is the AWS solution for establishing **dedicated network** connections from on-premises locations to AWS.

**Very fast network**:

- Lower Bandwidth 50M - 500M
- Higher Bandwidth 1GB or 10 GB

Benefits:

- Help **reduce network costs** and **increase bandwidth throughput**. (great for high traffic networks)
- Provides a **more consistent network experience** than a typical internet-based connection. (reliable and secure)

## VPC Endpoints Introduction

Think of a secret tunnel where you don't have to leave the AWS Network.

There are **two types** of VPC Endpoints:

1. **Interface Endpoint**
2. **Gateway Endpoint**

VPC Endpoints allow you to **privately connect your VPC to other AWS services**.

VPC endpoint services can:

- Eliminate the need for an **Internet Gateway**, **NAT device**, **VPN connection**, or **AWS Direct Connect** connections.
- Instance in the VPC **do not require a public IP address** to communicate with service resource.
- Traffic between your VPC and other services **does not leave the AWS network**.
- **Horizontally scaled**, **redundant**, and **highly available** VPC component.
- Allow secure communication between instances and services **without adding availability risks or bandwidth constraints** on your traffic.

## VPC Interface Endpoints

**Internet Endpoints** are **Elastic Network Interfaces (ENI)** with a **private IP address**.

They serve as an entry point for traffic going to a supported service.

Interface Endpoints are powered by **AWS PrivateLink**, access services hosted on AWS easily and securely by keeping your network traffic within the AWS network.

Interface Endpoints support the following **AWS Services**:

- API Gateway
- CloudFormation
- CloudWatch
- Kinesis
- SageMaker
- Codebuild
- AWS Config
- EC2 API
- ELB API
- AWS KMS
- Secrets Manager
- Security Token Service
- Service Catalog
- SNS
- SQS
- Systems Manager
- Marketplace Partner Services
- Endpoint Services in other AWS accounts

## VPC Gateway Endpoints

A **Gateway Endpoint** is a gateway that is a target for **a specific route** in your **route table**, used for traffic destined for a supported AWS service.

To create a Gateway Endpoint, you must specify the VPC in which you want to create the endpoint, and the service to which you want to establish the connection.

Gateway Endpoints current supports 2 service:

- Amazon S3
- DynamoDB
