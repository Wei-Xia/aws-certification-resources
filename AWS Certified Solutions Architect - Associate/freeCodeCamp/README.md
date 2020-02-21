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
  - [S3 - Cross Region Replication (CRR )](#s3---cross-region-replication--crr--)
  - [S3 - Versioning](#s3---versioning)
  - [S3 - Lifecycle Management](#s3---lifecycle-management)
  - [S3 - Transfer Acceleration](#s3---transfer-acceleration)
  - [S3 - Presigned URLs](#s3---presigned-urls)
  - [S3 - MFA Delete](#s3---mfa-delete)
  - [S3 - Cheat Sheet](#s3---cheat-sheet)
- [Snowball](#snowball)
  - [Introduction to Snowball](#introduction-to-snowball)
    - [Snowball features and limitations](#snowball-features-and-limitations)
  - [Snowball Edge](#snowball-edge)
    - [Snowball features and limitations](#snowball-features-and-limitations-1)
  - [Snowmobile](#snowmobile)
    - [Security Features](#security-features)
  - [Snowball - Cheat Sheet](#snowball---cheat-sheet)
- [Virtual Private Cloud](#virtual-private-cloud)
  - [Core Components](#core-components)
  - [VPC Key Features](#vpc-key-features)
  - [Default VPC](#default-vpc)
  - [Default Everywhere IP](#default-everywhere-ip)
  - [VPC Peering](#vpc-peering)
  - [VPC Route Tables](#vpc-route-tables)
  - [VPC Internet Gateway (IGW)](#vpc-internet-gateway--igw-)
  - [VPC Bastion / Jumpbox](#vpc-bastion---jumpbox)
  - [VPC Direct Connect](#vpc-direct-connect)
  - [VPC Endpoints Introduction](#vpc-endpoints-introduction)
  - [VPC Interface Endpoints](#vpc-interface-endpoints)
  - [VPC Gateway Endpoints](#vpc-gateway-endpoints)
  - [VPC Flow Logs Introduction](#vpc-flow-logs-introduction)
  - [VPC Network Access Control List Introduction](#vpc-network-access-control-list-introduction)
  - [VPC NACLs Use Case](#vpc-nacls-use-case)
  - [VPC Security Groups Introduction](#vpc-security-groups-introduction)
  - [VPC Security Groups Limits](#vpc-security-groups-limits)
  - [VPC Security Groups Use Case](#vpc-security-groups-use-case)
  - [VPC Network Address Translation (NAT)](#vpc-network-address-translation--nat-)
  - [VPC NAT Instances VS NAT Gateways](#vpc-nat-instances-vs-nat-gateways)
  - [VPC Cheat Sheet](#vpc-cheat-sheet)
    - [Endpoint Cheat Sheet](#endpoint-cheat-sheet)
    - [Flow Logs Cheat Sheet](#flow-logs-cheat-sheet)
    - [NACLs Cheat Sheet](#nacls-cheat-sheet)
    - [Security Group Cheat Sheet](#security-group-cheat-sheet)
    - [NAT Instance and NAT Gateway Cheat Sheet](#nat-instance-and-nat-gateway-cheat-sheet)

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

Object contains your data. They are like files.

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

## VPC Flow Logs Introduction

**VPC Flow Logs** allow you to capture **IP traffic information** in-and-out of Network Interfaces with your VPC.

All log data is **stored** using **Amazon CloudWatch Logs**. After a flow log is created, it can be viewed in detail within CloudWatch Logs.

Flow logs can be created for:

1. **VPC**
2. **Subnets**
3. **Network Interface**

## VPC Network Access Control List Introduction

An optional layer of security that acts as a **virtual firewall** for controlling traffic **in and out of subnets**.

![004](./assets/004.jpg)

VPCs automatically get a default NACL.

Each NACL contains a set of tules that can **allow** or **deny** traffic **into (inbound) nad out of (outbound) subnets**.

**Rule #** determines the **order of evaluation**. From lowest to highest. The highest rule # can be 32766 and its recommended to work in 10 or 100 increments.

You can allow or deny traffic. You could **block a single IP address** (You can't do this with Security Group).

## VPC NACLs Use Case

![005](./assets/005.jpg)

- We determine there is a malicious actor at a specific IP address is trying to access our instances so we **block their IP**.
- We never need to SSH into instances so we add a **DENY for these subnets**. This is just an additional measure in case our Security Groups SSH port was left open.

## VPC Security Groups Introduction

A virtual firewall that controls the traffic to and from EC2 instance.

Security Groups are associated with EC2 instances.

![006](./assets/006.jpg)

Each Security Group contains a set of rules that filter traffic coming **into(inbound)** and **out of (outbound)** EC2 instances by providing security at the **protocol** and **port** access level.

There are no **_DENY_** rules. **All traffic is blocked** by default unless a rule specifically allows it.

**Multiple Instances** across multiple subnets can belong to a **Security Group**.

## VPC Security Groups Limits

- You can have up to **10,000 Security Groups in a Region** (default is 2,500)
- You can have **60 inbound rules** and **60 outbound rules** per security group
- **16 Security Groups** per ENI - Elastic Network Interface (default is 5)

## VPC Security Groups Use Case

![007](./assets/007.jpg)

- You can specify the source to be an IP range or A specific IP (/32 is a specific IP address)
- You can specify the source to be another security group
- An instance be **belong to multiple Security Groups**, and rules are **permissive** (instead of restrictive). Meaning if you have one security group which has no Allow and you add an allow to another than it will Allow

## VPC Network Address Translation (NAT)

Network Address Translation (NAT) is the method of **re-mapping** one IP address space into another.

![008](./assets/008.jpg)

If you have a private network and you need to help gain outbound access to the internet you would need to use a NAT gateway to remap the Private IPs.

If you have two networks which have conflicting network addresses you can use a NAT to make the addresses more agreeable.

## VPC NAT Instances VS NAT Gateways

NATs have to run within a **Public Subnet**.

![009](./assets/009.jpg)

⤴️ **NAT Instances** (legacy) are individual EC2 instances. Community AMIs exist to launch NAT Instances.

![010](./assets/010.jpg)

⤴️ **NAT Gateway** is a manged service which launches redundant instances within the selected AZ.

## VPC Cheat Sheet

### Endpoint Cheat Sheet

- VPC Endpoints help keep traffic between AWS Services **within the AWS Network**
- There are two kinds of VPC Endpoints: Interface Endpoints and Gateway Endpoints
- Interface Endpoints **cost money**, Gateway Endpoints are **free**
- Interface Endpoints uses an Elastic Network Interface (ENI) with Private IP (powered by AWS PrivateLink)
- Gateway Endpoints is a target for a specific route in your route table
- Interface Endpoints support many AWS services
- Gateway Endpoints only support DynamoDB and S3

### Flow Logs Cheat Sheet

- **VPC Flow Logs** monitor the in-and-out traffic of your Network Interfaces with your VPC
- You can turn on Flow Logs at the VPC, Subnets, or Network Interface level
- VPC Flow Logs **cannot be tagged** like other AWS resources
- You **can not change the configuration** of a flow log **after it's created**
- You **can not enable** flow logs for VPCs which are peered with your VPC **unless it is in the same account**
- VPC Flow Logs can be delivered to an **S3** or **CloudWatch Logs**
- VPC Flow Logs contains the source and destination **IP addresses** (not hostname)
- Some instance traffic is **not monitored**:
  - Instance traffic generated by contacting the AWS DNS servers
  - Windows license activation traffic from instances
  - Traffic to and from the instance metadata address (169.254.169.254)
  - DHCP Traffic
  - Any traffic to the reserved IP address of the default VPC router

### NACLs Cheat Sheet

- Network Access Control List is commonly known as NACL
- VPCs are automatically given a default NACL which allow **all outbound and inbound** traffic
- Each subnet with a VPC must be associated with a NACL
- Subnets can only be associated with 1 NACL at a time. Associating a subnet with a new NACL will remove the previous association
- If a NACL is not explicitly associated with a subnet, the subnet will automatically be associated with the default NACL
- NACL has inbound and outbound rules, just like Security Groups
- Rule can either **allow** or **deny** traffic, unlike Security Groups which can only allow
- NACLs are STATELESS, which means any allowed inbound traffic is also allowed outbound
- When you create a NACLs, it will deny all traffic by default
- NACLs contain a numbered list of rules that gets evaluated in order from lowest to highest
- If you needed a block a single IP address, you could via NACLs (Security Groups cannot deny)

### Security Group Cheat Sheet

- Security Groups acts as a firewall at the instance level
- Unless allowed specifically, all **inbound traffic** is **blocked by default**
- All **Outbound traffic** from the instance is **allowed by default**
- You can specific for the source to be either an IP range, single IP Address or another security group
- Security Groups are **STATEFUL** (if traffic is allowed inbound, then it is also allowed outbound)
- Any changes to a Security Group take effect immediately
- EC2 Instances can belong to multiple security groups
- Security groups can contain multiple EC2 Instances
- You **cannot block specific IP addresses** with Security Groups, for this you would need a Network Access Control List (NACL)
- You can have up to 10,000 Security Groups per Region (default is 2,500)
- You can have 60 inbound and 60 outbound rules per Security Group
- You can have 16 Security Group associated to an ENI (default is 5)

### NAT Instance and NAT Gateway Cheat Sheet

- When creating a NAT instance you **must disable source and destination checks** on the instance
- NAT instances **must exist in a public subnet**
- You must have a **route out** of the private subnet to the NAT instance
- The size of a NAT instance determines **how much traffic can be handled**
- **High availability** can be achieved using **Autoscaling Groups**, multiple **subnets in different AZs**, and **automate failover between them using a script**.
- NAT Gateways are **redundant inside an Availability Zone** (can survive failure of EC2 instance)
- You can only have **1 NAT Gateway inside 1 Availability Zone** (cannot span AZs)
- Starts at 5 Gbps and scales all the way up to 45 Gbps
- NAT Gateways are the **preferred setup for enterprise systems**
- There is **no requirement to patch NAT Gateways**, and there is **no need to disable Source/Destination checks** for the NAT Gateway (unlike NAT Instances)
- NAT Gateways are **automatically assigned a public IP address**
- **Route Tables** for the NAT Gateway MUST be updated
- Resources in multiple AZs sharing a Gateway will **lose internet access if the Gateway** goes down, unless you create a **Gateway in each AZ** and configure **route tables** accordingly

# Identity Access Management (IAM)

## IAM Core Component

IAM allows **management** of access of **users** and **resource**

### IAM Identities

- IAM **Users**: End users who log into the console or interact with AWS resource programmatically
- IAM **Groups**: Group up your Users so they all share permission levels of the group eg. Administrators, Developers, Auditors
- IAM **Roles**: Associate permissions to a Role and then assign this to an Users or Groups

### IAM Policies

JSON documents which grant permissions for a specific user, group, or role to access services. Policies are **attached to the IAM Identities**.

### Use case

![011](./assets/011.jpg)

- A user can belong to a group. Roles can be applied to groups to quickly add and remove permissions en-masse to users
- A user can have a role directly attached. An policy can be directly attached to a user (called an **Inline Policy**)
- Roles can have many policies attached
- Various AWS resources allow you attache roles directly to them

## IAM Types of Policies

- **Managed Policies**: A policy which is managed by AWS, which you cannot edit. Managed policies are labeled with an orange box.
- **Customer Managed Policies**: A policy created by the customer which is editable. Customer policies have no symbol beside them.
- **Inline Policies**: A policy which is directly attached to the users.

## IAM Policies Structure

Policies Example:

```JSON
{
  "Version": "2012-10-17",
  "Statement": [{
      "Sid": "Deny-Barclay-S3-Access",
      "Effect": "Allow",
      "Action": [
        "s3:ListAllMyBuckets"
      ],
      "Resource": "arn:aws:s3:::*"
    },
    {
      "Effect": "Allow",
      "Action": [
        "s3:ListBucket",
        "s3:GetBucketLocation"
      ],
      "Resource": "arn:aws:s3:::examplebucket",
      "Condition": {
        "NumericLessThanEquals": {
          "aws:MultiFactorAuthAge": "3600"
        }
      }
    },
    {
      "Effect": "Allow",
      "Action": [
        "s3:PutObject",
        "s3:PutObjectAcl",
        "s3:GetObject",
        "s3:GetObjectAcl",
        "s3:DeleteObject"
      ],
      "Resource": "arn:aws:s3:::examplebucket/*",
      "Condition": {
        "NumericLessThanEquals": {
          "aws:MultiFactorAuthAge": "3600"
        }
      }
    }
  ]
}
```

- **Version**: Policy language version. `2012-10-17` is the latest version
- **Statement**: container for the policy element you are allowed to have multiples
- **Sid(optional)**: a way of labeling your statements
- **Effect**: Set whether the policy will `Allow` or `Deny`
- **Principal**: account, user, role or federated user to which you would like to allow or deny access
- **Action**: list of actions that the policy allows or denies
- **Resource**: the resource to which the action(s) applies
- **Condition(optional)**: circumstances under which the policy grants permission.

## IAM Password Policy

![012](./assets/012.jpg)

In IAM you can set a **Password Policy** to set the minimum requirements of a password and **rotate** passwords so users have to update their passwords after certain days.

## IAM Programmatic Access Keys

Access Keys allow users to interact with AWS service **programmatically** via the **AWS CLI** or **AWS SDK**.

You're allowed **two** Access Keys per user.

## IAM Multi-Factor Authentication

Multi-factor authentication (MFA) can be turned on per user.

The user has to turn on MFA **themselves**, Administrator **cannot directly enforce** users to have MFA.

The Administrator account could **create a policy** requiring MFA to access certain resources.

## IAM Cheat Sheet

# Amazon Cognito

## Amazon Cognito Introduction

Decentralized Managed **Authentication**.

Sign-up, Sign-in integration for your apps. Social identity provider eg. Facebook, Google.

![013](./assets/013.jpg)

- **Cognito User Pools**: User directory with authentication to Identity Provider (IpD) to grant access to your app
- **Cognito Identity Pools**: Provide temporary credentials for users to access AWS Services
- **Cognito Sync**: Syncs user data and preferences across all devices
