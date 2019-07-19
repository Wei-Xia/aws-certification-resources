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
