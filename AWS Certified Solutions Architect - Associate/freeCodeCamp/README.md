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
