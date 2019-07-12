1. Which of the following can be used to control access to your Amazon EC2 instances?

`EC2 Security groups`

Security groups are used to define and control the way you want your instances to be accessed, and whether or not certain kind of communications is allowed. AWS security groups provide security at the protocol and port access level. You can add rules to each security group that allow traffic to or from its associated instances.

2. A company is planning to introduce a new product to their customers. They are expecting high traffic to their web application. As part of the Enterprise support plan, which of the following could provide them with architectural and scaling guidance?

`Infrastructure Event Management`

AWS Infrastructure Event Management is a short-term engagement with AWS Support, included in the Enterprise-level Support product offering, and available for additional purchase for Business-level Support subscribers. AWS Infrastructure Event Management partners with your technical and project resources to gain a deep understanding of your use case and provide architectural and scaling guidance for an event. Common use-case examples for AWS Event Management include advertising launches, new product launches, and infrastructure migrations to AWS.

3. What are the benefits provided by the AWS Personal Health Dashboard? (Choose two)

`Personalized View of Service Health & Detailed Troubleshooting Guidance`

AWS Personal Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you. While the Service Health Dashboard displays the general status of AWS services, Personal Health Dashboard gives you a personalized view into the performance and availability of the AWS services underlying your AWS resources.

The benefits of the AWS personal health dashboard include:

A personalized View of Service Health: Personal Health Dashboard gives you a personalized view of the status of the AWS services that power your applications, enabling you to quickly see when AWS is experiencing issues that may impact you. For example, in the event of a lost EBS volume associated with one of your EC2 instances, you would gain quick visibility into the status of the specific service you are using, helping save precious time troubleshooting to determine root cause.

Proactive Notifications: The dashboard also provides forward looking notifications, and you can set up alerts across multiple channels, including email and mobile notifications, so you receive timely and relevant information to help plan for scheduled changes that may affect you. In the event of AWS hardware maintenance activities that may impact one of your EC2 instances, for example, you would receive an alert with information to help you plan for, and proactively address any issues associated with the upcoming change.

Detailed Troubleshooting Guidance: When you get an alert, it includes remediation details and specific guidance to enable you to take immediate action to address AWS events impacting your resources. For example, in the event of an AWS hardware failure impacting one of your EBS volumes, your alert would include a list of your affected resources, a recommendation to restore your volume, and links to the steps to help you restore it from a snapshot. This targeted and actionable information reduces the time needed to resolve issues.

4. You have 2 accounts in AWS. One for Dev and the other for QA. All are part of consolidated billing. The master account has purchased 4 reserved instances. The Dev department is currently using 2 reserved instances. The QA team is planning on using 3 instances, which are of the same instance type. What is the pricing tier of the instances that can be used by the QA Team?

`two reserved and one on-demand`

For billing purposes, the consolidated billing feature of AWS Organizations treats all the accounts in the organization as one account. This means that all accounts in the organization can receive the hourly cost benefit of Reserved Instances that are purchased by any other account. Since 2 reserved instances are already used by the Dev team , then there are another 2 instances that can be used by the QA team. The rest of the instances can be on-demand instances. Therefore the correct answer is 2 reserved and 1 on-demand.

5. According to the AWS Acceptable Use Policy, penetration testing of EC2 instances:

`May be performed by the customer on their own instances without prior authorization from AWS.`

AWS customers are welcome to carry out security assessments and penetration tests against their AWS infrastructure without prior approval for 8 services:

- Amazon EC2 instances, NAT Gateways, and Elastic Load Balancers.

- Amazon RDS.

- Amazon CloudFront.

- Amazon Aurora.

- Amazon API Gateways.

- AWS Lambda and Lambda Edge functions.

- Amazon Lightsail resources.

- Amazon Elastic Beanstalk environments.

6. You noticed that several critical Amazon Elastic Compute Cloud (Amazon EC2) instances have been terminated. Which of the following AWS services would help you determine who took this action?

`AWS CloudTrail`

AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting.

7. A company has decided to migrate to the AWS Cloud. AWS offers a wide range of services and instance types. They want to reduce costs as much as possible. Which of the following is the main factor to consider when choosing the instance type of services like Amazon RDS and Amazon Redshift?

`Workload utilization CPU and RAM`

AWS offers a broad range of resource types and configurations to suit a plethora of use cases. For example, services like Amazon EC2, Amazon RDS, Amazon Redshift, and Amazon Elasticsearch Service(Amazon ES) give you a lot of choice of instance types. In some cases, you should select the cheapest type that suits your workload’s requirements. In other cases, using fewer instances of a larger instance type might result in lower total cost or better performance. You should benchmark and select the right instance type depending on how your workload utilizes CPU, RAM, network, storage size, and I/O.

8. Select TWO examples of the AWS shared controls.

`Patch Management and Configuration Management`

Shared Controls are controls which apply to both the infrastructure layer and customer layers, but in completely separate contexts or perspectives. In a shared control, AWS provides the requirements for the infrastructure and the customer must provide their own control implementation within their use of AWS services.

Examples include:

- Patch Management – AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications.

- Configuration Management – AWS maintains the configuration of its infrastructure devices, but a customer is responsible for configuring their own guest operating systems, databases, and applications.

- Awareness & Training - AWS trains AWS employees, but a customer must train their own employees.

9. A company is deploying a new two-tier web application in AWS. Where should the most frequently accessed data be stored so that the application’s response time is optimal?

`Amazon ElastiCache`

Amazon ElastiCache is a web service that makes it easy to deploy, operate, and scale an in-memory data store or cache in the cloud. The service improves the performance of web applications by allowing you to retrieve information from fast, managed, in-memory data stores, instead of relying entirely on slower disk-based databases.

10. Which of the following services allows you to manage your agreements with AWS?

`AWS Artifact`

AWS Artifact is a self-service audit artifact retrieval portal that provides our customers with on-demand access to AWS’ compliance documentation and AWS agreements. You can use AWS Artifact Reports to download AWS security and compliance documents, such as AWS ISO certifications, Payment Card Industry (PCI), and System and Organization Control (SOC) reports. You can use AWS Artifact Agreements to review, accept, and track the status of AWS agreements such as the Business Associate Addendum (BAA).

11. A company has developed an eCommerce web application and the application needs an uptime of at least 99.5%. Which of the following deployment strategies should they use?

`Deploying the application across multiple Regions`

The AWS Global infrastructure is built around Regions and Availability Zones (AZs). Each AWS Region is a separate geographic area. Each AWS Region has multiple, isolated locations known as Availability Zones. Availability Zones in a region are connected with low latency, high throughput, and highly redundant networking. These Availability Zones offer AWS customers an easier and more effective way to design and operate applications and databases, making them more highly available, fault tolerant, and scalable than traditional single datacenter infrastructures or multi-datacenter infrastructures.

In addition to replicating applications and data across multiple data centers in the same Region using Availability Zones, you can also choose to increase redundancy and fault tolerance further by replicating data between geographic Regions (especially if you are serving customers from all over the world). You can do so using both private, high speed networking and public internet connections to provide an additional layer of business continuity, or to provide low latency access across the globe.

12. One of the benefits of the AWS Cloud is that there are many services available to use of which you don’t need to manage their underlying infrastructure. Which of the following are examples of these services? (Choose TWO)

`Amazon Elastic MapReduce and DynamoDB`

The Amazon Elastic MapReduce and DynamoDB are managed services that you don’t need to manage their underlying infrastructure. Other managed services include: Amazon S3, Amazon RDS, Amazon Redshift, Amazon WorkSpaces, Amazon CloudFront, Amazon CloudSearch and several other services.

13. A company has a DevOps team in its organizational structure. They are looking forward to moving to the AWS Cloud. They are wondering if there is an AWS service that can help them manage infrastructure as code. Which of the following would you suggest for them?

`AWS CloudFormation`

AWS CloudFormation is a service that helps you model and set up your Amazon Web Services resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and AWS CloudFormation takes care of provisioning and configuring those resources for you. You don't need to individually create and configure AWS resources and figure out what's dependent on what; AWS CloudFormation handles all of that.

14. A company is planning to develop an application consisting of hundreds of microservices. They decide to host the application on the AWS Cloud. Since there are a large number of services produced by the application, it needs a powerful tool for analysis and debugging. Which of the following services can best meet this requirement?

`AWS X-Ray`

AWS X-Ray helps developers analyze and debug production, distributed applications, such as those built using a microservices architecture. With X-Ray, you can understand how your application and its underlying services are performing to identify and troubleshoot the root cause of performance issues and errors. X-Ray provides an end-to-end view of requests as they travel through your application, and shows a map of your application’s underlying components. You can use X-Ray to analyze both applications in development and in production, from simple three-tier applications to complex microservices applications consisting of thousands of services.

15. A user is planning to host a scalable, dynamic web application on AWS. Which service may not be required by the user to achieve automated scalability?

`S3`

The user can achieve automated scalability by configuring the AutoScaling service to run the required number of EC2 instances based on the conditions that you define. Cloudwatch is used to monitor the utilization of the running instances and allow AutoScaling to automatically scale up (by launching more instances) or down (by terminating instances) based on changes on demand.

Based on the application requirements, a developer may decide not to use S3. The storage resource in this case will be the EBS volumes that are attached to the Amazon EC2 instances.

16. Your company is developing a critical application and the security of the application is one of the top priorities. Which of the following AWS services will provide infrastructure security optimization recommendations?

`AWS Trusted Advisor`

AWS Trusted Advisor is an online resource to help you reduce cost, increase performance, and improve security by optimizing your AWS environment. Trusted Advisor provides real time guidance to help you provision your resources following AWS best practices.

17. You have developed a web application that has a “.NET layer” that connects to a MySQL database. Which of the following AWS database deployments would provide automated backups to your application?

`Amazon Aurora`

Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud. Amazon Aurora combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. It delivers up to five times the throughput of standard MySQL and up to three times the throughput of standard PostgreSQL. Amazon Aurora is designed to be compatible with MySQL and with PostgreSQL, so that existing applications and tools can run without requiring modification. It is available through Amazon Relational Database Service (RDS), freeing you from time-consuming administrative tasks such as provisioning, patching, backup, recovery, failure detection, and repair.

18. A company has decided to migrate to AWS. What design principles should they consider to facilitate good design in the cloud?

`Automate to make architectural experimentation easier.`

The Well-Architected Framework identifies a set of general design principles to facilitate good design in the cloud:

- Stop guessing your capacity needs: Eliminate guessing about your infrastructure capacity needs. When you make a capacity decision before you deploy a system, you might end up sitting on expensive idle resources or dealing with the performance implications of limited capacity. With cloud computing, these problems can go away. You can use as much or as little capacity as you need, and scale up and down automatically.

- Test systems at production scale: In the cloud, you can create a production-scale test environment on demand, complete your testing, and then decommission the resources. Because you only pay for the test environment when it's running, you can simulate your live environment for a fraction of the cost of testing on premises.

- Automate to make architectural experimentation easier: Automation allows you to create and replicate your systems at low cost and avoid the expense of manual effort. You can track changes to your automation, audit the impact, and revert to previous parameters when necessary.

- Allow for evolutionary architectures: Allow for evolutionary architectures. In a traditional environment, architectural decisions are often implemented as static, one-time events, with a few major versions of a system during its lifetime. As a business and its context continue to change, these initial decisions might hinder the system's ability to deliver changing business requirements. In the cloud, the capability to automate and test on demand lowers the risk of impact from design changes. This allows systems to evolve over time so that businesses can take advantage of innovations as a standard practice.

- Drive architectures using data: In the cloud you can collect data on how your architectural choices affect the behavior of your workload. This lets you make fact-based decisions on how to improve your workload. Your cloud infrastructure is code, so you can use that data to inform your architecture choices and improvements over time.

- Improve through game days: Test how your architecture and processes perform by regularly scheduling game days to simulate events in production. This will help you understand where improvements can be made and can help develop organizational experience in dealing with events.

19. You are working on a project that involves creating thumbnails of millions of images; however, consistent uptime is not really an issue, and continuous processing is not required. Which type of EC2 buying option would be the most cost-effective?

`Spot Instances`

Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if you don't mind if your applications get interrupted. For example, Spot Instances are well-suited for data analysis, batch jobs, background processing, and optional tasks.

20. You are trying to organize and import gigabytes of data into AWS that are currently structured in JSON-like, name-value documents. Which AWS service would best fit your needs?

`DynamoDB`

DynamoDB is AWS' NoSQL database offering. NoSQL databases are used for non-structured data that are typically stored in JSON-like, name-value documents.

21. A company is currently using the Enterprise Support plan. They want quick and efficient guidance with their billing and account inquiries. Which of the following included services could assist them?

`AWS Support Concierge`

Included as part of the Enterprise Support plan, the Support Concierge Team are AWS billing and account experts that specialize in working with enterprise accounts. The Concierge team will quickly and efficiently assist you with your billing and account inquiries, and work with you to help implement billing and account best practices so that you can focus on running your business.

Support Concierge service includes:

- 24 x7 access to AWS billing and account inquires.

- Guidance and best practices for billing allocation, reporting, consolidation of accounts, and root-level account security.

- Access to Enterprise account specialists for payment inquiries, training on specific cost reporting, assistance with service limits, and facilitating bulk purchases.

22. An organization has decided to reserve EC2 compute capacity for three years to get more discounts. Their application workloads are likely to change during this time period. What is the EC2 Reserved Instance (RI) type that allows them to change the attributes of the RI whenever they need?

`Convertible RIs`

Convertible RIs provide a discount (up to 54% off On-Demand) and the capability to change the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value. These attributes include instance family, instance type, platform, scope, and tenancy.

23. The principle “design for failure and nothing will fail” is very important when designing your AWS Cloud architecture. Which of the following would help adhere to this principle? (Choose two)

`Availability Zones and Elastic Load Balancer`

Each AWS Region is a separate geographic area. Each AWS Region has multiple, isolated locations known as Availability Zones. When designing your AWS Cloud architecture, you should make sure that your system will continue to run even if failures happen. You can achieve this by deploying your AWS resources in multiple Availability zones. Availability zones are isolated from each other, therefore if one availability zone goes down, the other AZ’s will still be up and running and hence your application will be more fault tolerant. In addition to availability zones you can build a disaster recovery solution by deploying your AWS resources in other regions. If an entire region goes down you will still have resources in another region able to continue to provide a solution. Finally, you can use the Elastic Load Balancer to regularly perform health checks and distribute traffic only to the healthy instances.

24. You are going to create snapshots from EBS volumes in another geographical location using the console. Where would you create the snapshots?

`In another Region`

Since you are going to create snapshots in another geographical location then you will create them in another AWS Region.

25. One of the most important AWS best practices to follow is the cloud architecture principle of elasticity. How does following this principle improve your architecture’s design?

`By automatically provisioning the required AWS resources based on changes in demand.`

The concept of Elasticity involves the ability of a service to automatically scale its resources up or down based on changes in demand. For example, Amazon EC2 Autoscaling can help automate the process of adding or removing Amazon EC2 instances as demand increases or decreases.

25. Which of the following allows you to carve out a portion of the AWS Cloud?

`Amazon VPC`

Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined. This virtual network closely resembles a traditional network that you'd operate in your own data center, with the benefits of using the scalable infrastructure of AWS.
