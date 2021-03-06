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

26. What are two advantages of using Cloud Computing over using traditional data centers? (Choose two)

`Eliminating SPOFs and Distributed infrastructure`

These are things that a traditional web host cannot provide:

- High-availability (eliminating SPOFs: single points of failure): AWS makes the process of designing a highly available system simple and easy. A system is highly available when it can withstand the failure of an individual component or multiple components, such as hard disks, servers, and network links. The best way to understand and avoid the single point of failure is to begin by making a list of all major points of your architecture. You need to break the points down and understand them further. Then, review each of these points and think what would happen if any of these failed. AWS gives you the opportunity to automate recovery and reduce disruption at every layer of your architecture.

- Distributed infrastructure: The AWS Cloud spans 61 Availability Zones within 20 geographic regions around the world, with announced plans for 12 more Availability Zones and four more AWS Regions allowing you to reduce latency to users from all around the world.

- On-demand infrastructure for scaling applications or tasks: AWS allows you to provision the required resources for your application in minutes and also allows you to stop them when you don’t need them.

- Cost savings: You don't have to run your own data center for internal or private servers, so your IT department doesn't have to make bulk purchases of servers which may never get used, or may be inadequate. The “pay as you go” model from AWS allows you to pay only for what you use and the ability to scale down to avoid over-spending. With AWS you don't have to pay an entire IT department to maintain that hardware -- you don't even have to pay an accountant to figure out how much hardware you can afford or how much you need to purchase.

27. What is the feature provided by AWS that enables fast and secure transfer of files over long distances between your client and your Amazon S3 bucket?

`Amazon S3 Transfer Acceleration`

Amazon S3 Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path.

28. A company currently uses VM Templates to spin up virtual machines on their on-premise infrastructure. Which of the following can be used in a similar way to spin up EC2 instances on the AWS Cloud?

`Amazon Machine Image (AMI)`

An Amazon Machine Image (AMI) provides the information required to launch an EC2 instance, which is a virtual server in the cloud. You specify an AMI when you launch an instance, and you can launch as many instances from the AMI as you need. You can also launch instances from as many different AMIs as you need.

29. Which of the following AWS security features is associated with a subnet in a VPC and functions to filter incoming traffic requests?

`NACL`

A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You might set up network ACLs with rules similar to your security groups in order to add an additional layer of security to your VPC.

30. Which of the following AWS Cloud services is designed with native Multi-AZ fault tolerance in mind?

`Amazon DynamoDB and Amazon S3`

- Amazon DynamoDB runs across AWS proven, high-availability data centers. The service replicates data across three facilities in an AWS region to provide fault tolerance in the event of a server failure or Availability Zone outage.

- Amazon S3 provides durable infrastructure to store important data and is designed for durability of 99.999999999% of objects. Your data is redundantly stored across multiple facilities and multiple devices in each facility.

31. Which Cloud Computing model removes the need for your organization to manage operating systems?

`PaaS`

Platform as a Service (PaaS) removes the need for your organization to manage the underlying infrastructure (usually hardware and operating systems) and allows you to focus on the deployment and management of your applications. This helps you be more efficient as you don’t need to worry about resource procurement, capacity planning, software maintenance, patching, or any of the other undifferentiated heavy lifting involved in running your application.

32. Which of the following services can help protect your web applications from SQL injection and other vulnerabilities in your application code?

`AWS WAF`

AWS WAF (Web Application Firewall) helps protect your web applications from common web exploits that could affect application availability, compromise security, or consume excessive resources. You can use AWS WAF to create custom rules that block common attack patterns, such as SQL injection or cross-site scripting, and rules that are designed for your specific application.

33. Under the Shared Responsibility Model, which of the following are controls which a customer fully inherits from AWS? (Choose two)

`Physical Controls and Environmental Controls`

Inherited Controls are controls which a customer fully inherits from AWS such as physical controls and environmental controls.

34. Which of the following is NOT a feature of an edge location?

`Distributes load across multiple resources`

The Edge location does not distribute load. It is used in conjunction with the Cloudfront service to cache common responses and deliver content to end users with low latency. The AWS service that is used to distribute load is the ELB service.

35. Which of the following features of RDS allows for data redundancy across regions and improves disaster recovery?

`Creating Read Replicas`

Amazon RDS Read Replicas provide enhanced performance and durability for database (DB) instances. This feature makes it easy to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads. You can create one or more replicas of a given source DB Instance and serve high-volume application read traffic from multiple copies of your data, thereby increasing aggregate read throughput. In addition to that creating Read Replicas across regions improves your disaster recovery capabilities and allows you to scale out globally.

36. Which of the following services allows you to run containerized applications on a cluster of EC2 instances?

`Amazon Elastic Container Service (Amazon ECS)`

Amazon Elastic Container Service (Amazon ECS) is a highly scalable, high-performance container orchestration service that supports Docker containers and allows you to easily run and scale containerized applications on AWS. Amazon ECS eliminates the need for you to install and operate your own container orchestration software, manage and scale a cluster of virtual machines, or schedule containers on those virtual machines.

37. What information is required to calculate the Total Cost of Ownership for the AWS Cloud?

`The number of on-premise virtual machines`

The AWS TCO (Total Cost of Ownership) Calculator provides directional guidance on possible realized savings when deploying AWS. This tool is built on an underlying calculation model, that generates a fair assessment of value that a customer may achieve given the data provided by the user which includes the number of servers migrated to AWS, the server type, the number of processors and so on.

38. What services/features are required to maintain a highly available and fault-tolerant architecture in AWS?

`Amazon EC2 Auto Scaling and Elastic Load Balancer`

Amazon EC2 Auto Scaling continually monitors the utilization of the instances underlying your application to make sure that your application always has the right amount of compute. In other words Amazon EC2 Auto Scaling automatically scales the instances up during demand spikes (to increase the availability of the application) or scales them down when demand lulls (to minimize costs). In addition to that, Amazon EC2 Auto Scaling can detect when an instance is unhealthy, terminate it, and replace it with a new one which increases the “Fault Tolerance” of your application.

Elastic Load Balancing provides an effective way to increase the availability and fault tolerance of a system. First ELB tries to discover the availability of your EC2 instances, it periodically sends pings, attempts connections, or sends requests to test the EC2 instances. These tests are called health checks. The status of the instances that are healthy at the time of the health check is InService. The status of any instances that are unhealthy at the time of the health check is OutOfService. The load balancer routes user requests only to the healthy instances. When the load balancer determines that an instance is unhealthy, it stops routing requests to that instance. The load balancer resumes routing requests to the instance when it has been restored to a healthy state.

39. A company is hosting a web application in the AWS Cloud using a set of EC2 instances. Which of the following can help to protect them from DDoS attacks? (Choose two)

`Using Security Groups and Using Network Access Control Lists`

A security group acts as a virtual firewall for your instance to control inbound and outbound traffic.

A network access control list (ACL) acts as a firewall for controlling traffic in and out of one or more subnets. Therefore if they configured properly, they can protect your instances from DDoS attacks.

40. A company created a solution that will help AWS customers improve their architectures on AWS. Which AWS program may support this company?

`APN Consulting Partners`

APN Consulting Partners are professional services firms that help customers design, architect, build, migrate, and manage their workloads and applications on AWS. Consulting Partners include System Integrators, Strategic Consultancies, Agencies, Managed Service Providers, and Value-Added Resellers. AWS supports the APN Consulting Partners by providing a wide range of resources and training to support their customers.

41. You have developed a microservices-based application. Which of the following should you use to make sure that each EC2 instance in the system gets the same amount of traffic?

`Application Loader Balancer`

Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and Lambda functions. Elastic Load Balancing offers three types of load balancers: 1- Application Load Balancer. 2- Network Load Balancer. 3- Classic Load Balancer. Application Load Balancer is best suited for load balancing of HTTP and HTTPS traffic. In our case, the microservices application receives HTTP or HTTPS traffic. Hence, the Application Load Balancer is the correct answer here.

42. Your company is planning to host its applications in the AWS Cloud. Which of the following services can be used to help decouple distributed software systems and components? (Choose two)

`AWS SQS and AWS SNS`

Amazon Simple Queue Service (SQS) and Amazon SNS are both messaging services within AWS, which provide different benefits for developers.

Amazon SNS allows applications to send time-critical messages to multiple subscribers through a “push” mechanism, eliminating the need to periodically check or “poll” for updates.

Amazon SQS is a message queue service used by distributed applications to exchange messages through a polling model. Amazon SQS provides flexibility for distributed components of applications to send and receive messages without requiring each component to be concurrently available.

Using SNS, you can publish messages to Amazon SQS queues to reliably send messages to one or many system components asynchronously.

In brief, SQS and SNS can be integrated together to decouple application components so that they run (or fail ) independently, increasing the overall fault tolerance of the system.

43. Which of the following will impact the price paid for an EC2 instance? (Choose two)

`Instance Type and Storage Capacity`

EC2 instance pricing varies depending on many variables:

- The buying option (On-demand, Reserved, Spot, Dedicated)

- Selected AMI

- Selected instance type

- Region

- Data Transfer in/out

- Storage capacity.

44. Which of the following is a fully-managed, petabyte-scale data warehouse service in the AWS Cloud?

`Amazon Redshift`

Amazon Redshift is a fully managed, petabyte-scale data warehouse service in the cloud. You can start with just a few hundred gigabytes of data and scale to a petabyte or more. This enables you to use your data to acquire new insights for your business and customers.

45. Your company's upper management is getting very nervous about managing governance, compliance, and risk auditing in AWS. What service should you enable and inform upper management about?

`CloudTrail`

AWS CloudTrail is designed to log all actions taken in your AWS account. This provides a great resource for governance, compliance, and risk auditing.

46. Which of the following AWS services can be used as a compute resource? (Choose two)

`Amazon EC2 and AWS Lambda`

Although there are no servers to manage in AWS Lambda, this does not mean that there are no servers or compute resources doing the work. Every application needs compute capacity to run. With Lambda, AWS handles this compute capacity and manages it for you. In brief, AWS Lambda provides serverless computing in the AWS Cloud.

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud.

47. You are planning to offload some of your batch processing workloads to AWS. These jobs can be interrupted and resumed at any time. Which of the following instance types would be the most cost effective to use?

`Spot`

Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if your applications can be interrupted. For example, Spot Instances are well-suited for data analysis, batch jobs, background processing, and optional tasks.

48. Which of the following reserved instance payment options result in you paying a discounted hourly rate throughout the duration of the term? (Choose two)

`Partial Upfront option and No Upfront option`

You can choose between three payment options when you purchase a Standard or Convertible Reserved Instance:

- No Upfront: No upfront payment is required. You are billed a discounted hourly rate for every hour within the term, regardless of whether the Reserved Instance is being used. No Upfront Reserved Instances are based on a contractual obligation to pay monthly for the entire term of the reservation. A successful billing history is required before you can purchase No Upfront Reserved Instances.

- Partial Upfront: A portion of the cost must be paid up front and the remaining hours in the term are billed at a discounted hourly rate, regardless of whether you’re using the Reserved Instance.

- All Upfront: With the All Upfront option, you pay for the entire Reserved Instance term with one upfront payment. This option provides you with the largest discount compared to On-Demand instance pricing.

49. Which statement is correct with regards to service limits? (Choose two)

`You can use AWS Trusted Advisor to monitor your service limits, and You can contact support to increase the service limit`

Understanding your service limits (and how close you are to them) is an important part of managing your AWS deployments – continuous monitoring allows you to request limit increases or shut down resources before the limit is reached. One of the easiest ways to do this is via AWS Trusted Advisor’s Service Limit Dashboard, which currently covers 39 limits across 10 services.

AWS maintains service limits for each account to help guarantee the availability of AWS resources, as well as to minimize billing risks for new customers. Some service limits are raised automatically over time as you use AWS, though most AWS services require that you request limit increases manually. Most service limit increases can be requested through the AWS Support Center by choosing Create Case and then choosing Service Limit Increase.

50. What does Amazon Elastic Beanstalk provide?

`An application container on top of Amazon Web Services`

AWS Elastic Beanstalk makes it easy for developers to quickly deploy and manage applications in the AWS Cloud. Developers simply upload their application code, and Elastic Beanstalk automatically handles the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring.

51. Which of the following are important design principles when architecting cloud-based systems? (Choose two)

`Assume everything will fail, and Build loosely-coupled components`

Always design your application components to be loosely coupled. This is to ensure that even if one component fails, the entire system will not fail. Also if you design your system with the assumption that everything will fail, then you will ensure that the right measures are taken to build a highly available and fault tolerant system.

52. What is the primary storage service used by Amazon RDS DB instances?

`Amazon EBS`

DB instances for Amazon RDS for MySQL, MariaDB, PostgreSQL, Oracle, and Microsoft SQL Server use Amazon Elastic Block Store (Amazon EBS) volumes for database and log storage.

53. What are your options for protecting the confidentiality of data in transit in Amazon S3? (Choose two)

`using client-side encryption and Use SSL`

Data protection refers to protecting data while in-transit (as it travels to and from Amazon S3) and at rest (while it is stored on disks in Amazon S3 data centers). You can protect data in transit by using SSL or by using client-side encryption.

54. Which of the following AWS services are free to use? (Choose two)

`CloudFormation and Auto-scaling`

- AWS Auto Scaling is free to use: AWS Auto Scaling is a service that can help you optimize your utilization and cost efficiencies when consuming AWS services so you only pay for the resources you actually need. When demand drops, AWS Auto Scaling will automatically remove any excess resource capacity so you avoid overspending.

- AWS CloudFormation is available at no additional charge, and you pay only for the AWS resources needed to run your applications: AWS CloudFormation is a service that gives developers and businesses an easy way to create a collection of related AWS resources and provision them in an orderly and predictable fashion.

55. What service helps you to aggregate log files from your EC2 instances?

`CloudWatch Logs`

You can use Amazon CloudWatch Logs to monitor, store, and access your log files from Amazon Elastic Compute Cloud (Amazon EC2) instances, AWS CloudTrail, Route 53, and other sources. You can then retrieve the associated log data from CloudWatch Logs.

56. Select the services that can be used to build hybrid cloud architectures. (Choose two)

`AWS Identity and Access Management and Amazon Virtual Private Cloud`

In cloud computing, hybrid cloud refers to the use of both on-premises resources in addition to public cloud resources. A hybrid cloud enables an organization to migrate applications and data to the cloud, extend their datacenter capacity, utilize new cloud-native capabilities, move applications closer to customers, and create a backup and disaster recovery solution with cost-effective high availability. By working closely with enterprises, AWS has developed the industry’s broadest set of hybrid capabilities across storage, networking, security, application deployment, and management tools to make it easy for you to integrate the cloud as a seamless and secure extension of your existing investments.

AWS Identity and Access Management (IAM) can grant your employees and applications access to the AWS Management Console and AWS service APIs using your existing identity systems. AWS IAM supports federation from corporate systems like Microsoft Active Directory, as well as external Web Identity Providers like Google and Facebook.

Amazon Virtual Private Cloud (Amazon VPC) allows you to create a Hardware VPN connection between your corporate data center and your VPC to leverage the AWS Cloud as an extension of your corporate datacenter.

57. What are the benefits of using DynamoDB? (Choose two)

`Automatic scaling to meet required throughput capacity and single-digit millisecond latency`

Benefits of DynamoDB include:

- Performance at scale: DynamoDB supports some of the world’s largest scale applications by providing consistent, single-digit millisecond response times at any scale. You can build applications with virtually unlimited throughput and storage.
- Serverless: With DynamoDB, there are no servers to provision, patch, or manage and no software to install, maintain, or operate. DynamoDB automatically scales tables up and down to adjust for capacity and maintain performance.
- Highly available:Availability and fault tolerance are built in, eliminating the need to architect your applications for these capabilities.

58. Which of the following should you consider when creating a tagging strategy for your AWS resources? (Choose two)

`Use as many tags as possible to help filter your resource easily AND Always use a case-sensitive format for tags`

When creating a tagging strategy for AWS resources, make sure that it accurately represents organizationally relevant dimensions and adheres to the following tagging best practices:

- Always use a standardized, case-sensitive format for tags, and implement it consistently across all resource types.

- Consider tag dimensions that support the ability to manage resource access control, cost tracking, automation, and organization.

- Implement automated tools to help manage resource tags.

- Err on the side of using too many tags rather than too few tags.

- Remember that it is easy to modify tags to accommodate changing business requirements, however consider the ramifications of future changes, especially in relation to tag-based access control, automation, or upstream billing reports.

59. Which of the following support plans include the AWS Support Concierge Service?

`Enterprise`

Only the Enterprise plan includes the AWS Support Concierge Service.

60. You want to take a snapshot of an EC2 Instance and create a new instance out of it. This snapshot is equivalent to:

`AMI`

An Amazon Machine Image (AMI) provides the information required to launch an instance, which is a virtual server in the cloud. You must specify an AMI when you launch an instance, and you can launch as many instances from the AMI as you need. You can also launch instances from as many different AMIs as you need.

61. You have been asked to set up a database in AWS that will require frequent updates. You know that you will need a reasonable amount of storage space but are unsure of the best option. Which type of storage should be used by a database instance based on the above criteria?

`Amazon EBS`

Amazon EBS provides durable, block-level storage volumes that you can attach to a running Amazon EC2 instance. Amazon EBS volumes offer consistent and low-latency performance compared to other storage options. You can use EBS volumes as primary storage for data that requires frequent updates, such as the system drive for an instance or storage for a database application.

62. Which AWS support plan would help provide general guidance when you request Architecture Support?

`Developer`

The developer support plan provides general guidance when you request Architecture Support.

63. Which of the following are benefits of the AWS's Relational Database Service (RDS)? (Choose two)

`Automated patches and backups, You can resize capacity accordingly`

Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching and backups. It frees you to focus on your applications so you can give them the fast performance, high availability, security and compatibility they need.

64. What are design principles for performance efficiency in the cloud? (Choose two)

`Use serverless architectures, Go global in minutes`

There are five design principles for performance efficiency in the cloud:

- Democratize advanced technologies: Technologies that are difficult to implement can become easier to consume by pushing that knowledge and complexity into the cloud vendor's domain. Rather than having your IT team learns how to host and run a new technology, they can simply consume it as a service. For example, NoSQL databases, media transcoding, and machine learning are all technologies that require expertise that is not evenly dispersed across the technical community. In the cloud, these technologies become services that your team can consume while focusing on product development rather than resource provisioning and management.

- Go global in minutes: Easily deploy your system in multiple Regions around the world with just a few clicks. This allows you to provide lower latency and a better experience for your customers at minimal cost.

- Use serverless architectures: In the cloud, serverless architectures remove the need for you to run and maintain servers to carry out traditional compute activities. For example, storage services can act as static websites, removing the need for web servers, and event services can host your code for you. This not only removes the operational burden of managing these servers, but also can lower transactional costs because these managed services operate at cloud scale.

- Experiment more often: With virtual and automatable resources, you can quickly carry out comparative testing using different types of instances, storage, or configurations.

- Mechanical sympathy: Use the technology approach that aligns best to what you are trying to achieve. For example, consider data access patterns when selecting database or storage approaches.

65. What does AWS offer to secure your network? (Choose two)

`Built-in firewall, Encrypt data in transit`

AWS has a Built-in firewall that can be used to control traffic to your network.

You can secure your network by encrypting your data in transit with TLS across all services.

66. Which of the following is a benefit of running an application in multiple Availability Zones?

`Increase the availability of your application`

Placing instances that run your application in multiple Availability Zones improves the fault tolerance of your application. If one Availability Zone experiences an outage, traffic is routed to another Availability Zone, and this will increase the availability of your application.

67. Which of the following allows you to create a new RDS instance? (Choose two)

`AWS Management Console, AWS CloudFormation`

The AWS Management Console lets you create a new RDS instance through a web-based user interface.

You can also use the AWS CloudFormation service to create a new RDS instance using the CloudFormation template language.

68. Which of the following statements best describes the AWS shared controls?

`Controls which apply to both the infrastructure layer and customer layers`

Shared Controls are controls which apply to both the infrastructure layer and customer layers, but in completely separate contexts or perspectives. In a shared control, AWS provides the requirements for the infrastructure and the customer must provide their own control implementation within their use of AWS services. Examples include:

- Patch Management – AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications.

- Configuration Management – AWS maintains the configuration of its infrastructure devices, but a customer is responsible for configuring their own guest operating systems, databases, and applications.

- Awareness & Training - AWS trains AWS employees, but a customer must train their own employees.

69. How can ELBs improve the fault tolerance of your application?

`By ensuring that only healthy targets receive traffic`

ELB continuously performs health checks on the registered targets (such as Amazon EC2 instances) and only routes traffic to the healthy ones. This increases the fault tolerance of your application and makes it highly available.

70. Which of the following AWS services can help you perform security analysis and compliance auditing? (Choose two)

`AWS Config, AWS Inspector`

With AWS Config, you can discover existing and deleted AWS resources, determine your overall compliance against rules, and dive into configuration details of a resource at any point in time. These capabilities enable compliance auditing, security analysis, resource change tracking, and troubleshooting.

Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. Amazon Inspector automatically assesses applications for exposure, vulnerabilities, and deviations from best practices. This allows you to make security testing a more regular occurrence as part of development and IT operations.

Additional information:

One of the most important services that can help you perform security analysis and compliance auditing is AWS CloudTrail. AWS CloudTrail simplifies your compliance audits by automatically recording and storing event logs for actions made within your AWS account. With AWS CloudTrail, you can discover and troubleshoot security and operational issues by capturing a comprehensive history of changes that occurred in your AWS account within a specified period of time.

71. How does AWS Lambda work?

`Just upload your code and watch it run`

AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume - there is no charge when your code is not running. With Lambda, you can run code for virtually any type of application or backend service - all with zero administration. Just upload your code and Lambda takes care of everything required to run and scale your code with high availability. You can set up your code to automatically trigger from other AWS services or call it directly from any web or mobile app.

72. You want to quickly deploy your .NET application on the AWS Cloud. Which of the following AWS services can best help you?

`AWS Elastic Beanstalk`

AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

73. Which of the following are customer responsibilities when using EC2? (Choose two)

`Install and configure third-party software, Protect sensitive data`

Amazon EC2 requires the customer to perform all of the necessary security configuration and management tasks. When customers deploy Amazon EC2 instances, they are responsible for management of custom Amazon Machine Images, management of the guest operating systems (including updates and security patches), securing application access and data, installing and configuring third-party applications or utilities, and the configuration of the AWS-provided firewall (called a security group) on each instance.

74. What are AWS’ recommendations regarding root access keys?

`Delete them`

AWS recommends that you delete your root access keys because you can’t restrict permissions for the root user credentials. If you want to manage services that require administrative access create an IAM user, grant administrator access to that user, then use those credentials to interact with AWS.

75. Which of the following services help reduce the complexity and time needed to plan your application migration to the AWS Cloud?

`AWS Application Discovery Service`

AWS Application Discovery Service helps systems integrators quickly and reliably plan application migration projects by automatically identifying applications running in on-premises data centers, their associated dependencies, and their performance profiles. Planning data center migrations can involve thousands of workloads that are often deeply interdependent. Application discovery and dependency mapping are important early first steps in the migration process, but these tasks are difficult to perform at scale due to the lack of automated tools.AWS Application Discovery Service automatically collects configuration and usage data from servers, storage, and networking equipment to develop a list of applications, how they perform, and how they are interdependent. This information is retained in encrypted format in an AWS Application Discovery Service database, which you can export as a CSV or XML file into your preferred visualization tool or cloud migration solution to help reduce the complexity and time in planning your cloud migration.

76. For managed services like Amazon DynamoDB, what are the security-related tasks that AWS is responsible for? (Choose two)

`Install antivirus software, Disaster recovery`

AWS has increased responsibilities for its managed services. Examples of managed services include Amazon DynamoDB, Amazon RDS, Amazon Redshift, Amazon Elastic MapReduce, and Amazon WorkSpaces. These services provide the scalability and flexibility of cloud-based resources with less operational overhead because AWS handle basic security tasks like guest operating system (OS) and database patching, installing antivirus software, and disaster recovery. For most managed services, you only configure logical access controls and protect account credentials, while maintaining control and responsibility of any personal data.

77. You need to set up a security certificate for a client's eCommerce website in order to use the HTTPS protocol. Which of the following AWS services do you need to access in order to manage your SSL server certificate? (Choose two)

`AWS Identity & Access Management, AWS ACM`

To enable HTTPS connections to your website or application in AWS, you need an SSL/TLS server certificate. You can use a server certificate provided by AWS Certificate Manager (ACM) or one that you obtained from an external provider. You can use ACM or IAM to store and deploy server certificates. Use IAM as a certificate manager only when you must support HTTPS connections in a region that is not supported by ACM. IAM supports deploying server certificates in all regions, but you must obtain your certificate from an external provider for use with AWS. Amazon Route 53 is used to register domain names or use your own domain name to route your end users to Internet applications. Route 53 is not responsible for creating SSL certifications.

78. Big Cloud Jumbo Corp is beginning to explore migrating their entire on-premises data center to AWS. They are very concerned about how much it will cost once their entire IT infrastructure is running on AWS. What tool would you recommend they use to perform a cost-benefit analysis of moving to the AWS Cloud?

`AWS TCO (Total Cost of Ownership) Calculator`

The AWS TCO (Total Cost of Ownership) Calculator is a free tool provided by AWS that allows you to compare your current on-premises cost vs. estimated AWS cost.

79. Doodle, Inc. has a web application that ultimately stores billions of images and videos. All told, there is almost an exabyte of data stored in Doodle’s system. Which of the following AWS services can best transfer the data to AWS?

`Snowmobile`

AWS Snowmobile is an Exabyte-scale data transfer service used to move extremely large amounts of data to AWS. You can transfer up to 100PB per Snowmobile, a 45-foot long ruggedized shipping container, pulled by a semi-trailer truck. Snowmobile makes it easy to move massive volumes of data to the cloud, including video libraries, image repositories, or even a complete data center migration. At exabyte scale, transferring data with Snowmobile is more secure, fast and cost effective.

80. Which of the following are use cases for Amazon S3? (Choose two)

`Hosting static websites, A media store for the CloudFront service`

You can host a static website on Amazon Simple Storage Service (Amazon S3). On a static website, individual webpages include static content. They might also contain client-side scripts. To host a static website, you configure an Amazon S3 bucket for website hosting, allow public read access, and then upload your website content to the bucket. By contrast, a dynamic website relies on server-side processing, including server-side scripts such as PHP, JSP, or ASP.NET. Amazon S3 does not support server-side scripting. Amazon Web Services (AWS) also has resources for hosting dynamic websites such as Amazon EC2.

Amazon S3 is an excellent storage facility for your media assets. It is infinitely scalable, has built-in redundancy, and is available to you on a pay-as-you-go basis. For example, if you want to deliver or stream video files to your global users, all you need to do is to put your content in an S3 bucket and create a CloudFront distribution that points to the bucket. Your user’s video player will use CloudFront URLs to request the video file. The request will be directed to the best edge location, based on the user’s location. The Amazon Cloudfront Content Delivery Network (CDN) will serve the video from its cache, fetching it from the S3 bucket if it has not already been cached. The CDN caches content at the edge locations for consistent, low-latency, high-throughput video delivery.

81. What are the main benefits of using the AWS Service Catalog?

`Centrally manage commonly deployed IT services`

AWS Service Catalog allows organizations to create and manage catalogs of IT services that are approved for use on AWS. These IT services can include everything from virtual machine images, servers, software, and databases to complete multi-tier application architectures. AWS Service Catalog allows you to centrally manage commonly deployed IT services, and helps you achieve consistent governance and meet your compliance requirements, while enabling users to quickly deploy only the approved IT services they need.

82. Which of the following statements describes the AWS Cloud’s agility?

`AWS allows you to provision resources in minutes`

In a cloud computing environment, new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes. This results in a dramatic increase in agility for the organization, since the cost and time it takes to experiment and develop is significantly lower.

83. What is the DynamoDB replication technology that provides fast, local, read/write performance for globally-deployed applications?

`Global Tables`

Global Tables builds upon DynamoDB’s global footprint to provide you with a fully managed, multi-region, and multi-master database that provides fast, local, read and write performance for massively scaled, global applications. Global Tables replicates your Amazon DynamoDB tables automatically across your choice of AWS regions. Multi-master replication ensures that updates performed in any region are propagated to other regions, and that data in all regions are eventually consistent. This means tables accessed locally by your globally distributed application are always up to date.

84. Due to the nature of the traditional infrastructure environments and their upfront cost model, they involve using fixed, long-running servers that can become problematic as heterogeneous system configurations emerge from continual changes and software patches being applied overtime. Which of the following approaches solves these problems in the AWS environment?

`Use disposable resources instead of fixed servers`

With the immutable infrastructure pattern, if a problem happens with a server (EC2 instance), rather than updating, it is replaced with a new server containing the latest patches and configuration.

85. Which of the following approaches can be used to automate the process of deploying new compute resources having the same configuration and the same state of a running resource? (Choose two)

`Use Bootstrapping, Use Golden Images`

Whether you are deploying a new environment for testing, or increasing capacity of an existing system to cope with extra load, you will not want to manually set up new resources with their configuration and code. It is important that you make this an automated and repeatable process that avoids long lead times and is not prone to human error. The following approaches can be used to achieve this:

- Bootstrapping: When you launch an AWS resource like an Amazon EC2 instance or Amazon Relational Database (Amazon RDS)DB instance, you start with a default configuration. You can then execute automated bootstrapping actions. That is, scripts that install software or copy data to bring that resource to a particular state. You can parameterize configuration details that vary between different environments (e.g.,production, test, etc.) so that the same scripts can be reused without modifications.

- Golden Images: Certain AWS resource types like Amazon EC2instances, Amazon RDS DB instances, Amazon Elastic Block Store (Amazon EBS) volumes, etc., can be launched from a golden image: a snapshot of a particular state of that resource. When compared to the bootstrapping approach, a golden image results in faster start times and removes dependencies to configuration services or third-party repositories. This is important in auto-scaled environments where you want to be able to quickly and reliably launch additional resources as a response to demand changes.

86. You have multiple accounts in AWS. Which of the following can be used to reduce costs?

`Consolidated Billing`

The Consolidated Billing feature is part of the “AWS organization” service. Once you add your multiple accounts to an Organization, AWS charges you based on a consolidated bill for all of the linked accounts. With Consolidated Billing, you can see a combined view of AWS charges incurred by all accounts, as well as get a cost report for each individual account associated with your payer account. For billing purposes, AWS treats all the accounts in the organization as if they were one account. Some services, such as Amazon EC2 and Amazon S3, have volume pricing tiers across certain usage dimensions that give you lower prices the more you use the service. With consolidated billing, AWS combines the usage from all accounts to determine which volume pricing tiers to apply, giving you a lower overall price whenever possible.

87. Which services does AWS offer for free? (Choose two)

`Elastic Beanstalk, AWS IAM`

AWS Identity and Access Management is a feature of your AWS account offered at no additional charge. You will be charged only for use of other AWS services by your Users.

There is no additional charge for AWS Elastic Beanstalk. You pay for AWS resources (e.g. EC2 instances or S3 buckets) you create to store and run your application. You only pay for what you use, as you use it; there are no minimum fees and no upfront commitments.

88. Which of the following can be used to process a large number of binary files while following the AWS well-architected design principles?

`Use a number of parallel EC2 instance`

One of the most important design principles is to “scale horizontally to increase aggregate system availability”. Replace one large resource with multiple small resources to reduce the impact of a single failure on the overall system. For example if you want to convert a large number of binary files to text files or if you want to transcode large number of video files to another format, it is recommended that you use multiple EC2 instances in parallel instead of using one large instance.

89. What should you do if you see resources, which you don’t remember creating, in the AWS Management Console? (Choose two)

`Change your AWS root account password and the password of any IAM users, Delete any resources on your account you don't remember creating`

If you suspect that your account has been compromised, or if you have received a notification from AWS that the account has been compromised, perform the following tasks:

- Change your AWS root account password and the passwords of any IAM users.

- Delete or rotate all root and AWS Identity and Access Management (IAM) access keys.

- Delete any resources on your account you didn’t create, such as EC2 instances and AMIs, EBS volumes and snapshots, and IAM users.

- Respond to any notifications you received from AWS Support through the AWS Support Center.

90. What is a placement group in Amazon EC2?

`It is a group of EC2 instances within a single Availability Zone.`

Placement Groups are logical groupings or clusters of instances within a single Availability Zone. Placement groups are specifically used for launching cluster of compute instance types. Placement groups are recommended for applications that benefit from low network latency, high network throughput, or both.

91. Which of the following tools can be used to estimate your monthly bill?

`Simple Monthly Caculator`

The AWS Simple Monthly Calculator helps customers and prospects estimate their monthly AWS bill more efficiently. The calculator can be used to determine your best and worst case scenarios and identify areas of development to reduce your monthly costs and even compare it with other service providers who do not offer utility-style of billing (pay-as-you-go).

92. Which of the following services can be used to monitor the HTTP and HTTPS requests that are forwarded to Amazon CloudFront?

`AWS WAF`

AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to Amazon CloudFront or an Application Load Balancer. AWS WAF also lets you control access to your content by defining customizable web security rules.

93. Which of the following AWS services uses tiered pricing?

`AWS S3`

For S3 storage and data transfer OUT from EC2, AWS follows a tiered pricing model. Tiered pricing means that you pay less per unit when you use more. For example the more GBs you use in S3, the more you save.

94. For mobile applications, which of the following allows client devices access to AWS resources?

`Amazon Cognito`

Amazon Cognito provides solutions to control access to backend resources from your app. You can define roles and map users to different roles so your app can access only the resources that are authorized for each user.

95. AWS allows you to create a “Golden Environment”, where you can capture your security policies (such as firewall rules, network access controls, internal/external subnets, and operating system hardening), reuse it among multiple projects, and have it become part of your continuous integration pipeline. Which of the following AWS services is most involved in creating such an environment?

`AWS Cloud​Formation`

Traditional security frameworks, regulations, and organizational policies define security requirements related to things such as firewall rules, network access controls, internal/external subnets, and operating system hardening. You can implement these in an AWS environment as well, but you now have the opportunity to capture them all in a script that defines a “Golden Environment.” This means you can create an AWS CloudFormation script that captures your security policy and reliably deploys it. Security best practices can now be reused among multiple projects and become part of your continuous integration pipeline. You can perform security testing as part of your release cycle, and automatically discover application gaps and drift from your security policy. Additionally, for greater control and security, AWS CloudFormation templates can be imported as “products" into AWS Service Catalog. This enables centralized management of resources to support consistent governance, security, and compliance requirements, while enabling users to quickly deploy only the approved IT services they need.

96. Who can help your organization achieve their desired business outcomes with AWS?

`AWS Professional Services`

Adopting the AWS Cloud can provide you with sustainable business advantages. Supplementing your team with specialized skills and experience can help you achieve those results. The AWS Professional Services organization is a global team of experts that can help you realize your desired business outcomes when using the AWS Cloud.

97. You are developing a document generator application that helps users create and modify PDFs. Which of the following allows you to publish your application?

`AWS Serverless Application Repository`

AWS Serverless Application Repository is used to share solutions with developers or to help your customers quickly understand the value of products and services you sell and support. Anyone with an AWS account can publish a serverless application or application component to the AWS Serverless Application Repository. You can share your published applications within your team, across your organization, or with the community at large. Publicly shared applications must include a link to the application's source code so others can view what the application does and how it works.

98. What are the different types of identities in AWS? (Choose two)

`IAM Roles, IAM Users`

Identities on AWS include users (or groups) and roles. You create these identities on AWS to manage access to your AWS resources and determine the actions that each identity can perform on these resources.

99. Which pillar of the AWS Well-Architected Framework focuses on using infrastructure as code?

`Operational Excellence`

Using infrastructure as code is one of the most important design principles for operational excellence in the cloud. In the cloud, you can apply the same engineering discipline that you use for application code to your entire environment. You can define your entire workload (applications, infrastructure, etc.) as code and update it with code. You can script your operational procedures and automate their execution by triggering them in response to events. By performing operations as code, you limit human error and enable consistent responses to events.

100. Which of the following are advantages of using AWS as a cloud computing provider? (Choose two)

Advantages of Cloud Computing include:

- Trade capital for variable expense: Instead of having to invest heavily in data centers and servers before you know how you’re going to use them, you can only pay when you consume computing resources, and only pay for how much you consume.

- Benefit from massive economies of scale: By using cloud computing, you can achieve a lower variable cost than you can get on your own. Because usage from hundreds of thousands of customers are aggregated in the cloud, providers such as Amazon Web Services can achieve higher economies of scale which translates into lower pay as you go prices.

- Stop guessing capacity: Eliminate guessing on your infrastructure capacity needs. When you make a capacity decision prior to deploying an application, you often either end up sitting on expensive idle resources or dealing with limited capacity. With cloud computing, these problems go away. You can access as much or as little as you need, and scale up and down as required with only a few minutes notice.

- Increase speed and agility: In a cloud computing environment, new IT resources are only ever a click away, which means you reduce the time it takes to make those resources available to your developers from weeks to just minutes. This results in a dramatic increase in agility for the organization, since the cost and time it takes to experiment and develop is significantly lower.

- Stop spending money on running and maintaining data centers: Focus on projects that differentiate your business, not the infrastructure. Cloud computing lets you focus on your own customers, rather than on the heavy lifting of racking, stacking and powering servers.

- Go global in minutes: Easily deploy your application in multiple regions around the world with just a few clicks. This means you can provide a lower latency and better experience for your customers simply and at minimal cost.

101. Your organization heavily uses Chef to operate their configuration management systems. Which AWS Cloud service provides integration with Chef recipes to automate the configuration of servers across Amazon EC2 Instances?

`AWS OpsWorks`

AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet. Chef and Puppet are automation platforms that allow you to use code to automate the configurations of your servers. OpsWorks lets you use Chef and Puppet to automate how servers are configured, deployed, and managed across your Amazon EC2 instances or on-premises compute environments.

102. Which of the following is NOT a benefit of using Amazon VPC?

`Amazon VPC allows you to control user interactions with various AWS resources`

Amazon Virtual Private Cloud (Amazon VPC) lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including selection of your own IP address range, creation of subnets, and configuration of route tables and network gateways. Also, Subnets, IP ranges, route tables, and security groups are automatically created for you (default configurations), so you can concentrate on creating the applications to run in your VPC.

103. Where does one go to find and download AWS SOC& PCI reports?

`AWS Artifact`

AWS Artifact provides on-demand downloads of AWS security and compliance documents, such as AWS ISO certifications, Payment Card Industry (PCI), and Service Organization Control (SOC) reports. You can submit the security and compliance documents (also known as audit artifacts) to your auditors or regulators to demonstrate the security and compliance of the AWS infrastructure and services that you use. You can also use these documents as guidelines to evaluate your own cloud architecture and assess the effectiveness of your company's internal controls.

104. Which of the following are examples of the customer’s responsibility to implement “security in the cloud”? (Choose two)

`Build application's schema, Analyzing network performance`

"Security in the Cloud" refers to the Customer’s responsibility in the Shared Responsibility Model. Customers are responsible for items such as building application schema, analyzing network performance, configuring security groups and network ACLs, and encrypting their data.

"Security of the Cloud" refers to the AWS’ responsibility in the Shared Responsibility Model. AWS is responsible for items such as the physical security of the DC (data center), creating hypervisors, replacement of old disk drives, and patch management of the infrastructure.

105. Which of the following is the most cost-effective AWS service that can be used for long-term data backup and archiving?

`AWS Storage Gateway`

AWS Storage Gateway is a hybrid storage service that enables your on-premises applications to seamlessly use AWS cloud storage. You can use the service for backup and archiving, disaster recovery, cloud data processing, storage tiring, and migration. The gateway connects to AWS storage services, such as Amazon S3, Amazon S3 Glacier, Amazon S3 Glacier Deep Archive, Amazon EBS, and AWS Backup, providing storage for files, volumes, snapshots, and virtual tapes in AWS.

106. Your company uses on-demand EC2 Instances dedicated to a project that has just been canceled. The company does not want to incur charges for these on-demand Instances. However, it also does not want to lose the data yet because there is a chance the project may be revived in the next few days. What should you do to minimize charges for these Instances in the meantime?

`stop the instances as soon as possible`

The best way to minimize charges is to stop the instances to avoid any data transfer charges that the instance may incur if left running.

107. You are facing a lot of problems with your current contact center. Which service provides a cloud-based contact center that can deliver a better service for your customers?

`Amazon Connect`

Amazon Connect is a cloud-based contact center solution. Amazon Connect makes it easy to set up and manage a customer contact center and provide reliable customer engagement at any scale. You can set up a contact center in just a few steps, add agents from anywhere, and start to engage with your customers right away. Amazon Connect provides rich metrics and real-time reporting that allow you to optimize contact routing. You can also resolve customer issues more efficiently by putting customers in touch with the right agents. Amazon Connect integrates with your existing systems and business applications to provide visibility and insight into all of your customer interactions.

108. Which of the following services provide real-time auditing for compliance and vulnerabilities? (Choose three)

`AWS Config, Amazon Inspector, AWS Trusted Advisor`

Services like AWS Config, Amazon Inspector, and AWS Trusted Advisor continually monitor for compliance or vulnerabilities giving you a clear overview of which IT resources are in compliance, and which are not. With AWS Config rules you will also know if some component was out of compliance even for a brief period of time, making both point-in-time and period-in-time audits very effective.

109. Which of the following would you use to manage your encryption keys in the AWS Cloud? (Choose two)

`AWS KMS, Cloud HSM`

AWS Key Management Service (KMS) is a managed service that makes it easy for you to create and control the encryption keys used to encrypt your data, and uses FIPS 140-2 validated hardware security modules to protect the security of your keys. AWS Key Management Service is integrated with most other AWS services to help you protect the data you store with these services. AWS Key Management Service is also integrated with AWS CloudTrail to provide you with logs of all key usage to help meet your regulatory and compliance needs.

AWS CloudHSM is a cloud-based hardware security module (HSM) that enables you to easily generate and use your own encryption keys on the AWS Cloud. With CloudHSM, you can manage your own encryption keys using FIPS 140-2 Level 3 validated HSMs. CloudHSM offers you the flexibility to integrate with your applications using industry-standard APIs, such as PKCS#11, Java Cryptography Extensions (JCE), and Microsoft CryptoNG (CNG) libraries.

110. Which of the following is a cloud computing deployment model that connects infrastructure and applications between cloud-based resources and existing resources not located in the cloud ?

`Hybrid`

A hybrid deployment is a way to connect infrastructure and applications between cloud-based resources and existing resources that are not located in the cloud. The most common method of hybrid deployment is between the cloud and existing on-premises infrastructure to extend, and grow, an organization's infrastructure into the cloud while connecting cloud resources to the internal system.

111. Which of the following services can be used to build video analytics applications?

`Amazon Kinesis`

You can use Amazon Kinesis to securely stream video from camera-equipped devices in homes, offices, factories, and public places to AWS. You can then use these video streams for video playback, security monitoring, face detection, machine learning, and other analytics.

112. What does the term “Economies of scale” mean?

`It means that AWS will continuously lower costs as it grows`

By using cloud computing, you can achieve a lower variable cost than you would get on your own. Because usage from hundreds of thousands of customers is aggregated in the cloud, providers such as AWS can achieve higher economies of scale, which translates into lower pay as-you-go prices.

113. Which DynamoDB feature can be used to reduce the latency of requests to a database from milliseconds to microseconds?

`DAX`

Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers performance improvements from milliseconds to microseconds – even at millions of requests per second. DAX adds in-memory acceleration to your DynamoDB tables without requiring you to manage cache invalidation, data population, or cluster management.

114. Which of the following strategies help analyze costs in AWS?

`Using tags to group resources`

Tags are key-value pairs that allow you to organize your AWS resources into groups.

You can use tags to:

- Visualize information about tagged resources in one place, in conjunction with Resource Groups.

- View billing information using Cost Explorer and the AWS Cost and Usage report.

- Send notifications about spending limits using AWS Budgets.

It is recommended to use logical groupings of your resources that make sense for your infrastructure or business. You could organize your resources by: Project, Cost center, Development environment, Application or Department. For example, if you tag resources with an application name, you can track the total cost of a single application that runs on those resources.

115. What are some key benefits of using AWS CloudFormation? (Choose three)

The benefits of using AWS CloudFormation include:

- CloudFormation allows you to model your entire infrastructure in a text file. This template becomes the single source of truth for your infrastructure. This helps you to standardize infrastructure components used across your organization, enabling configuration compliance and faster troubleshooting.

- AWS CloudFormation provisions your resources in a safe, repeatable manner, allowing you to build and rebuild your infrastructure and applications, without having to perform manual actions or write custom scripts. CloudFormation takes care of determining the right operations to perform when managing your stack, and rolls back changes automatically if errors are detected.

- Codifying your infrastructure allows you to treat your infrastructure as just code. You can author it with any code editor, check it into a version control system, and review the files with team members before deploying into production.

- CloudFormation allows you to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts.

116. What are some key advantages of AWS Security? (Choose two)

The Benefits of AWS Security include :

- Keep Your Data Safe: The AWS infrastructure puts strong safeguards in place to help protect your privacy. All data is stored in highly secure AWS data centers.

- Meet Compliance Requirements: AWS manages dozens of compliance programs in its infrastructure. This means that segments of your compliance have already been completed.

- Save Money: Cut costs by using AWS data centers. Maintain the highest standard of security without having to manage your own facility.

- Scale Quickly: Security scales with your AWS Cloud usage. No matter the size of your business, the AWS infrastructure is designed to keep your data safe.

117. Which of the following resources are serverless? (Choose two)

`AWS Lambda, Amazon ECS`

AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume, and there is no charge when your code is not running. With Lambda, you can run code for virtually any type of application or backend service - all with zero administration. Just upload your code and Lambda takes care of everything required to run and scale your code with high availability.

Amazon ECS features AWS Fargate, so you can deploy and manage containers without having to provision or manage servers. With Fargate, you no longer have to select Amazon EC2 instance types, provision, and scale clusters of virtual machines to run containers or schedule containers to run on clusters and maintain their availability. Fargate enables you to focus on building and running applications, not managing the underlying infrastructure.

118. What does the AWS Storage Gateway provide?

`It allows one to integrate on premises IT environments with Cloud Storage`

AWS Storage Gateway connects an on-premises software appliance with cloud-based storage to provide seamless integration with data security features between your on-premises IT environment and the AWS storage infrastructure.

119. When dealing with Container Services AWS is responsible for: (Choose two)

`Managing the underlying infrastruture, Managing the application platform`

The AWS shared responsibility model also applies to container services, such as Amazon RDS and Amazon EMR. For these services, AWS manages the underlying infrastructure and foundation services, the operating system and the application platform. For example, Amazon RDS for Oracle is a managed database service in which AWS manages all the layers of the container, up to and including the Oracle database platform. For services such as Amazon RDS, the AWS platform provides data backup and recovery tools; but it is your responsibility to configure and use tools in relation to your business continuity and disaster recovery (BC/DR) policy. For AWS Container services, you are responsible for the data and for firewall rules for access to the container service. For example, Amazon RDS provides RDS security groups, and Amazon EMR allows you to manage firewall rules through Amazon EC2 security groups for Amazon EMR instances.

120. On the monthly statement, there is a section where you can see the charges for outbound data transfer. What is the name of that section?

`AWS Data Transfer Out`

Outbound data transfer is aggregated across services and then charged at the outbound data transfer rate. This charge appears on the monthly statement as AWS Data Transfer Out.

121. You need to migrate a large number of on-premises workloads to AWS. Which of the following is the fastest way to achieve your goal?

`Use the AWS Server Migration Service`

AWS Server Migration Service (SMS) is an agentless service which makes it easier and faster for you to migrate thousands of on-premises workloads to AWS. AWS SMS allows you to automate, schedule, and track incremental replications of live server volumes, making it easier for you to coordinate large-scale server migrations.

122. Which of the following are Amazon EC2 reserved instances types? (Select two)

There are three types of EC2 reserved instances(RIs) that you can choose from based on your applications needs:

- Standard RIs: These provide the most significant discount (up to 75% off On-Demand) and are best suited for steady-state usage.

- Convertible RIs: These provide a discount (up to 54% off On-Demand) and the capability to change the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value. Like Standard RIs, Convertible RIs are best suited for steady-state usage.

- Scheduled RIs: These are available to launch within the time windows you reserve. This option allows you to match your capacity reservation to a predictable recurring schedule that only requires a fraction of a day, a week, or a month.

123. You are sure that your application deployed in AWS needs frequent updates for the next 6 months. Which of the following services would allow you to make these updates easily, retaining the ability to change the AWS resources powering the application any time?

`AWS Elastic Beanstalk`

AWS Elastic Beanstalk is considered a Platform as a Service (PaaS). it is an easy-to-use service for deploying, scaling and updating web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS. You can simply upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. At the same time, you retain full control over the AWS resources powering your application and can access the underlying resources at any time.

124. Why are Serverless Architectures more economical than Server-based Architectures?

`With the Server-based Architectures, servers continue to run all the time but with the serverless architectures the code runs only when needed.`

Serverless architectures can reduce costs because you don’t have to manage or pay for underutilized servers, or provision redundant infrastructure to implement high availability. For example, you can upload your code to the AWS Lambda compute service, and the service can run the code on your behalf using AWS infrastructure. With AWS Lambda, you are charged for every 100ms your code executes and the number of times your code is triggered.

125. Select the services that are server-based: (Choose two)

Server-based services include: Amazon EC2, Amazon RDS, Amazon Redshift and Amazon EMR.

Serverless services include: AWS Lambda, AWS Fargate, Amazon ECS and Amazon DynamoDB.

126.  Who from the following will get the largest discount?

`A user who choose to buy Reserved, Standard, All upfront instances`

Reserved instance types include:

- Standard RIs: These provide the most significant discount (up to 75% off On-Demand) and are best suited for steady-state usage.

- Convertible RIs: These provide a discount (up to 54% off On-Demand) and the capability to change the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value.

Therefore, Standard RIs provides more discounts than Convertible RIs.

You can choose between three payment options when you purchase a Standard or Convertible Reserved Instance. With the All Upfront option, you pay for the entire Reserved Instance term with one upfront payment. With the Partial Upfront option, you make a low upfront payment and are then charged a discounted hourly rate for the instance for the duration of the Reserved Instance term. The No Upfront option does not require any upfront payment and provides a discounted hourly rate for the duration of the term.

Remember that when you buy Reserved Instances, the larger the upfront payment, the greater the discount.

- The All Upfront option provides you with the largest discount.

- The Partial Upfront option provides fewer discounts than All Upfront.

- The No Upfront option provides you with the least discount.
