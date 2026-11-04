# Cloud Engineering Handbook

A competency handbook for cloud and platform engineers working with AWS, Azure and Google Cloud. It pairs core cloud concepts with short, service-by-service answers on architecture, security, networking, serverless, containers, infrastructure as code, cost and migration. Use it for self-assessment, onboarding, design reviews and team skill mapping: read a topic, answer from your own experience first, then compare with the answer here and follow the official docs for depth.

1. [Cloud Computing Fundamentals](#cloud-computing-fundamentals)
2. [Amazon Web Services (AWS)](#amazon-web-services-aws)
    * [All AWS services with brief description](#list-of-aws-services-with-brief-description)
3. [Microsoft Azure](#microsoft-azure)
4. [Google Cloud Platform (GCP)](#google-cloud-platform-gcp)
5. [Contributing to This Repository](#contributing-to-this-repository)
6. [License](#license)

## About this handbook

Content is organized by provider: AWS, Microsoft Azure and Google Cloud (GCP) each have their own section, and the AWS section also lists services with a brief description. Answers are concise starting points, not complete references, so compare them with your own experience and consult the official AWS, Azure and Google Cloud documentation for depth. Service names and statuses were refreshed in 2026; the providers change them often, so check the docs before relying on a detail.

## Cloud Computing Fundamentals

Topics in this section:

1. [What is cloud computing, and what are its key characteristics?](#what-is-cloud-computing-and-what-are-its-key-characteristics)
2. [Explain the differences between IaaS, PaaS, and SaaS.](#explain-the-differences-between-iaas-paas-and-saas)
3. [What are the major cloud service providers, and what are their core services?](#what-are-the-major-cloud-service-providers-and-what-are-their-core-services)
4. [Essential components of a cloud architecture](#essential-components-of-a-cloud-architecture)
5. [Virtualization and cloud computing](#virtualization-and-cloud-computing)
6. [Cloud scalability and its benefits](#cloud-scalability-and-its-benefits)
7. [Cloud security and common challenges](#cloud-security-and-common-challenges)
8. [What is the difference between public, private, and hybrid clouds?](#what-is-the-difference-between-public-private-and-hybrid-clouds)
9. [Cloud data storage options and their use cases](#cloud-data-storage-options-and-their-use-cases)
10. [Data redundancy and disaster recovery](#data-redundancy-and-disaster-recovery)
11. [Advantages of serverless computing](#advantages-of-serverless-computing)
12. [How to handle data migration in the cloud](#how-to-handle-data-migration-in-the-cloud)
13. [Role of a reverse proxy in a cloud environment](#role-of-a-reverse-proxy-in-a-cloud-environment)
14. [Principles of cloud data warehousing](#principles-of-cloud-data-warehousing)
15. [Cloud bursting and when it is useful](#cloud-bursting-and-when-it-is-useful)
16. [How to monitor and manage cloud resource performance](#how-to-monitor-and-manage-cloud-resource-performance)
17. [Role of a Content Delivery Network (CDN)](#role-of-a-content-delivery-network-cdn)
18. [Significance of cloud monitoring and management tools](#significance-of-cloud-monitoring-and-management-tools)
19. [How auto-scaling works in cloud environments](#how-auto-scaling-works-in-cloud-environments)
20. [Cloud migration strategy and how to plan it](#cloud-migration-strategy-and-how-to-plan-it)
21. [Role of load balancers in the cloud](#role-of-load-balancers-in-the-cloud)
22. [Managing cloud resources using automation](#managing-cloud-resources-using-automation)
23. [Multi-cloud and its advantages and challenges](#multi-cloud-and-its-advantages-and-challenges)
24. [Principles of microservices architecture in the cloud](#principles-of-microservices-architecture-in-the-cloud)
25. [Cloud virtual private network (VPN)](#cloud-virtual-private-network-vpn)
26. [How do you secure cloud-based applications and data?](#how-do-you-secure-cloud-based-applications-and-data)
27. [Explain the concept of cloud networking and its components.](#explain-the-concept-of-cloud-networking-and-its-components)
28. [What is cloud billing and cost management?](#what-is-cloud-billing-and-cost-management)
29. [How do you achieve data backup and recovery in the cloud?](#how-do-you-achieve-data-backup-and-recovery-in-the-cloud)
30. [Describe the use of cloud-based databases.](#describe-the-use-of-cloud-based-databases)
31. [What are serverless functions, and when do you use them?](#what-are-serverless-functions-and-when-do-you-use-them)
32. [Role of Identity and Access Management (IAM) in the cloud](#role-of-identity-and-access-management-iam-in-the-cloud)
33. [Cloud application programming interface (API)](#cloud-application-programming-interface-api)
34. [How to troubleshoot cloud-based applications](#how-to-troubleshoot-cloud-based-applications)
35. [Use of containers in cloud computing](#use-of-containers-in-cloud-computing)
36. [How to ensure data encryption in the cloud](#how-to-ensure-data-encryption-in-the-cloud)
37. [Cloud Security Alliance (CSA)](#cloud-security-alliance-csa)
38. [Principles of disaster recovery in the cloud](#principles-of-disaster-recovery-in-the-cloud)
39. [How to choose the right cloud service model for a project](#how-to-choose-the-right-cloud-service-model-for-a-project)
40. [Cloud application architecture pattern](#cloud-application-architecture-pattern)
41. [Use of serverless databases in the cloud](#use-of-serverless-databases-in-the-cloud)
42. [How to implement high availability in a cloud infrastructure](#how-to-implement-high-availability-in-a-cloud-infrastructure)
43. [Role of cloud identity and access management](#role-of-cloud-identity-and-access-management)
44. [Continuous integration and continuous deployment (CI/CD) in the cloud](#continuous-integration-and-continuous-deployment-cicd-in-the-cloud)
45. [How to achieve data replication in the cloud](#how-to-achieve-data-replication-in-the-cloud)
46. [Cloud DNS service and how it works](#cloud-dns-service-and-how-it-works)
47. [Benefits of cloud serverless compute platforms](#benefits-of-cloud-serverless-compute-platforms)
48. [How to handle cloud storage security and access control](#how-to-handle-cloud-storage-security-and-access-control)
49. [Cloud architecture diagram and its importance](#cloud-architecture-diagram-and-its-importance)
50. [Principles of cloud compliance and auditing](#principles-of-cloud-compliance-and-auditing)
51. [How to design a resilient cloud architecture](#how-to-design-a-resilient-cloud-architecture)
52. [Cloud cost optimization and how to achieve it](#cloud-cost-optimization-and-how-to-achieve-it)
53. [Use of cloud-native application development](#use-of-cloud-native-application-development)
54. [How to manage cloud resources using Infrastructure as Code (IaC)](#how-to-manage-cloud-resources-using-infrastructure-as-code-iac)
55. [Cloud-native container orchestration platform](#cloud-native-container-orchestration-platform)
56. [Principles of cloud application performance tuning](#principles-of-cloud-application-performance-tuning)
57. [How to achieve data governance in the cloud](#how-to-achieve-data-governance-in-the-cloud)
58. [Role of cloud access control policies](#role-of-cloud-access-control-policies)
59. [Use of cloud-based message queues](#use-of-cloud-based-message-queues)
60. [How to design a cloud data warehouse](#how-to-design-a-cloud-data-warehouse)
61. [Cloud backup and recovery strategy](#cloud-backup-and-recovery-strategy)
62. [Principles of cloud load balancing](#principles-of-cloud-load-balancing)
63. [How to secure data transfer in a cloud environment](#how-to-secure-data-transfer-in-a-cloud-environment)
64. [Cloud disaster recovery planning](#cloud-disaster-recovery-planning)
65. [Use of cloud API gateways](#use-of-cloud-api-gateways)
66. [How to achieve cloud network segmentation](#how-to-achieve-cloud-network-segmentation)
67. [Role of a cloud management console](#role-of-a-cloud-management-console)
68. [Principles of cloud data archiving](#principles-of-cloud-data-archiving)
69. [How to manage cloud-based databases](#how-to-manage-cloud-based-databases)
70. [Cloud-native service mesh](#cloud-native-service-mesh)
71. [Use of cloud resource tagging](#use-of-cloud-resource-tagging)
72. [How to design a cloud content delivery strategy](#how-to-design-a-cloud-content-delivery-strategy)
73. [Cloud governance and policy enforcement](#cloud-governance-and-policy-enforcement)
74. [Principles of cloud application scaling](#principles-of-cloud-application-scaling)
75. [How to achieve compliance in a multi-cloud environment](#how-to-achieve-compliance-in-a-multi-cloud-environment)
76. [Role of cloud encryption at rest and in transit](#role-of-cloud-encryption-at-rest-and-in-transit)
77. [Use of cloud-based data lakes](#use-of-cloud-based-data-lakes)
78. [Cloud resource lifecycle management](#cloud-resource-lifecycle-management)
79. [Cloud security incident response plan](#cloud-security-incident-response-plan)
80. [Principles of cloud application monitoring](#principles-of-cloud-application-monitoring)
81. [How to ensure data privacy in the cloud](#how-to-ensure-data-privacy-in-the-cloud)
82. [Cloud network optimization](#cloud-network-optimization)
83. [Use of cloud-based container registries](#use-of-cloud-based-container-registries)
84. [Cloud access management strategy](#cloud-access-management-strategy)
85. [Cloud disaster recovery testing plan](#cloud-disaster-recovery-testing-plan)
86. [Principles of cloud application logging](#principles-of-cloud-application-logging)
87. [How to achieve cost transparency in the cloud](#how-to-achieve-cost-transparency-in-the-cloud)
88. [Role of cloud compliance reporting](#role-of-cloud-compliance-reporting)

### What is cloud computing, and what are its key characteristics?

**Cloud computing** is the on-demand delivery of computing services—including servers, storage, databases, networking, software, analytics, intelligence, and more—over the Internet ("the cloud") to offer faster innovation, flexible resources, and economies of scale.

### Key characteristics of cloud computing:

* **On-demand self-service:** Users can provision computing resources as needed without requiring human interaction with each service provider.
* **Broad network access:** Cloud services are accessible over the network and through standard devices.
* **Resource pooling:** The provider's computing resources are pooled to serve multiple customers with different physical and virtual resources dynamically assigned and reassigned according to customer demand.
* **Rapid elasticity:** Cloud services can be rapidly and elastically provisioned, in some cases automatically, to scale quickly up or down based on demand.
* **Measured service:** Cloud services are metered by the amount of resources consumed, such as compute time, storage, and network bandwidth.

### Explain the differences between IaaS, PaaS, and SaaS.

**Infrastructure as a service (IaaS)** is the most basic cloud service model. It provides access to computing resources, such as servers, storage, and networking. Users are responsible for managing and maintaining the resources, including installing and configuring operating systems and applications.

**Platform as a service (PaaS)** provides a platform for developing, running, and managing applications. It includes IaaS capabilities, plus additional services such as databases, middleware, and development tools. Users do not need to manage the underlying infrastructure, but they are still responsible for managing and maintaining their applications.

**Software as a service (SaaS)** is the most complete cloud service model. It provides access to software applications that are hosted and managed by the cloud provider. Users do not need to manage any infrastructure or applications; they simply access the applications through a web browser or mobile device.

### Comparison of IaaS, PaaS, and SaaS:

| Responsibility | IaaS | PaaS | SaaS |
|---|---|---|---|
| Data and access policies | You | You | You |
| Applications | You | You | Provider |
| Runtime, middleware, OS | You | Provider | Provider |
| Virtualization, servers, storage, networking | Provider | Provider | Provider |

### What are the major cloud service providers, and what are their core services?

The major cloud service providers are:

* Amazon Web Services (AWS)
* Microsoft Azure
* Google Cloud Platform (GCP)

These providers offer a wide range of cloud services, including IaaS, PaaS, and SaaS. Some of their core services include:

* **AWS:** Compute (EC2), storage (S3), databases (RDS), networking (VPC), analytics (Redshift), machine learning (SageMaker), and more.
* **Azure:** Compute (Virtual Machines), storage (Blob Storage), databases (SQL Database), networking (Virtual Network), analytics (Synapse Analytics), machine learning (Azure ML), and more.
* **GCP:** Compute (Compute Engine), storage (Cloud Storage), databases (Cloud SQL), networking (Cloud Networking), analytics (BigQuery), machine learning (Vertex AI), and more.

In addition to the major cloud providers, there are also a number of smaller and more specialized cloud providers. For example, some providers focus on specific industries, such as healthcare or financial services. Others focus on specific types of cloud services, such as machine learning or data analytics.

### Essential components of a cloud architecture

A cloud architecture is a design that describes how cloud computing components will be deployed and managed. It includes the following components:

* **Compute:** This component provides the processing power needed to run applications. It can be delivered as virtual machines (VMs), containers, or serverless functions.
* **Storage:** This component provides the space to store data and applications. It can be delivered as block storage, object storage, or file storage.
* **Networking:** This component provides the connectivity between the different components of a cloud architecture. It can be delivered as virtual private networks (VPNs), load balancers, and firewalls.
* **Management:** This component provides the tools and services needed to manage cloud resources. It can include billing, monitoring, and orchestration tools.

### Virtualization and cloud computing

Virtualization is the process of creating a virtual computer system (VM) on a physical computer. VMs can be used to run multiple applications on a single physical server, or to isolate applications from each other.

Virtualization is essential to cloud computing because it allows cloud providers to pool their resources and deliver them to multiple customers on demand. It also allows customers to easily scale their resources up or down as needed.

### Cloud scalability and its benefits

Cloud scalability is the ability of a cloud computing system to adapt to changing computing requirements by either increasing or decreasing its resources, such as computing power, storage, or network capacity on demand.

Cloud scalability has a number of benefits, including:

* **Cost savings:** Organizations can save money by scaling their cloud resources up or down as needed, instead of having to overprovision resources in anticipation of peak demand.
* **Improved performance:** Cloud scalability can help to improve the performance of applications by ensuring that they have the resources they need to run smoothly.
* **Increased agility:** Cloud scalability allows organizations to quickly respond to changes in demand by rapidly scaling their cloud resources up or down.
* **Enhanced business continuity:** Cloud scalability can help to improve business continuity by ensuring that applications are still available even if there is a problem with one of the underlying physical servers.

### Cloud security and common challenges

Cloud security is the practice of protecting cloud computing systems and data from unauthorized access, use, disclosure, disruption, modification, or destruction.

Some of the common cloud security challenges include:

* **Data breaches:** Data stored in the cloud is a common target. Exposed storage buckets and stolen credentials are frequent causes.
* **Misconfigurations:** Cloud resources can be misconfigured, which can expose them to attack.
* **Insider threats:** Malicious insiders can steal data or sabotage cloud systems.
* **Shared responsibility:** Cloud providers and customers share responsibility for cloud security. It is important for customers to understand their security responsibilities and to take steps to protect their data and applications.

### What is the difference between public, private, and hybrid clouds?

**Public cloud** services are shared by multiple organizations over the public internet. They are often the most cost-effective and scalable option, but they offer less control over the underlying infrastructure.

**Private cloud** services are dedicated to a single organization. They can be hosted on-premises or by a third-party provider. Private clouds offer more control and security than public clouds, but they are more expensive and less scalable.

**Hybrid clouds** combine public and private cloud services. This allows organizations to take advantage of the benefits of both cloud models, such as the scalability and cost-effectiveness of public clouds and the security and control of private clouds.

### Cloud data storage options and their use cases

The most common cloud data storage options are:

* **Block storage:** Block storage is designed for storing and accessing data in blocks, such as volumes and snapshots. It is commonly used for storing operating systems, databases, and other applications.
* **Object storage:** Object storage is designed for storing and accessing data as objects, such as files, images, and videos. It is commonly used for storing large volumes of data, such as backups, archives, and media content.
* **File storage:** File storage is designed for storing and accessing data in a hierarchical file system. It is commonly used for storing documents, spreadsheets, presentations, and other types of files.

### Use cases for cloud data storage:

* **Cloud backup and recovery:** Cloud data storage can be used to back up data from on-premises systems and applications. This data can then be restored to the on-premises systems in the event of a disaster.
* **Cloud archiving:** Cloud data storage can be used to archive old data that is no longer needed on a regular basis. This data can be easily accessed from the cloud when needed.
* **Cloud application development and hosting:** Cloud data storage can be used to store and host data and applications. This allows organizations to develop and deploy applications quickly and easily without having to invest in their own infrastructure.
* **Cloud content delivery:** Cloud data storage can be used to deliver content, such as images and videos, to users around the world. This allows organizations to scale their content delivery networks without having to invest in their own infrastructure.

### Data redundancy and disaster recovery

There are a number of ways to ensure data redundancy and disaster recovery in the cloud, including:

* **Replication:** Replication is the process of copying data to multiple locations. This can be done within a single cloud region or across multiple cloud regions.
* **Backups:** Backups are copies of data that can be restored in the event of a disaster. Backups can be stored in the cloud or on-premises.
* **Snapshots:** Snapshots are point-in-time copies of data. They can be used to restore data to a previous state in the event of a data loss or corruption.

### Advantages of serverless computing

Serverless computing is a cloud computing model in which the cloud provider automatically manages the server infrastructure. This allows developers to focus on writing code without having to worry about managing servers.

Some of the advantages of serverless computing include:

* **Scalability:** Serverless computing is highly scalable, so organizations can scale their applications up or down as needed without having to manage servers.
* **Cost savings:** Organizations only pay for the resources they use, so they can save money on server costs.
* **Ease of use:** Serverless computing is easy to use, so developers can focus on writing code without having to worry about managing servers.

### Cloud orchestration and its importance

Cloud orchestration is the process of automating the deployment, management, and scaling of cloud resources. It is important because it can help organizations to:

* **Reduce costs:** Cloud orchestration can help organizations to reduce costs by automating the management and scaling of cloud resources. This can help to prevent overprovisioning of resources and ensure that resources are used efficiently.
* **Improve agility:** Cloud orchestration can help organizations to improve agility by automating the deployment of new applications and services. This can help organizations to respond to changes in demand more quickly.
* **Increase reliability:** Cloud orchestration can help organizations to increase reliability by automating the monitoring and recovery of cloud resources. This can help to prevent outages and ensure that applications are always available.

### How to optimize costs in a cloud environment

There are a number of ways to optimize costs in a cloud environment, including:

* **Rightsizing:** Rightsizing is the process of ensuring that you are using the right amount of resources for your needs. This can be done by monitoring your resource usage and adjusting your resource allocation accordingly.
* **Reserved instances and savings plans:** Reserved Instances (AWS), Reservations (Azure), and Savings Plans (AWS and Azure) offer a discount in exchange for a one-year or three-year commitment. Committed pricing is typically cheaper than on-demand.
* **Spot instances:** Spot Instances (AWS) and Spot VMs (Azure) are spare capacity sold at a discount. The provider can reclaim them at short notice, so use them for interruptible workloads such as batch processing jobs.
* **Discounts:** Cloud providers offer a variety of discounts, such as volume discounts and discounts for committed use.

### Infrastructure as Code (IaC)

Infrastructure as Code (IaC) is the practice of managing and provisioning infrastructure using code. IaC tools allow you to define your infrastructure in a text file and then use that file to create and manage your infrastructure.

IaC is important because it allows you to:

* **Automate your infrastructure:** IaC can help you to automate the deployment, management, and scaling of your infrastructure. This can save you time and money, and it can also help to reduce errors.
* **Version control your infrastructure:** IaC allows you to version control your infrastructure, which means that you can track changes to your infrastructure over time. This can help you to troubleshoot problems and to roll back changes if necessary.
* **Make your infrastructure more portable:** IaC makes it easy to move your infrastructure between different cloud providers or to on-premises environments. This can give you more flexibility and control over your infrastructure.

### DevOps in the cloud

DevOps is a set of practices that combine software development (Dev) and IT operations (Ops) into a single team. The goal of DevOps is to automate the software development and deployment process, so that software can be released more quickly and reliably.

DevOps is important in the cloud because it can help organizations to:

* **Release software more quickly:** DevOps can help organizations to release software more quickly by automating the software development and deployment process. This can help organizations to stay ahead of the competition and to meet the demands of their customers.
* **Improve the quality of software:** DevOps can help organizations to improve the quality of software by automating testing and by integrating testing into the software development process. This can help to reduce the number of bugs in software and to improve the overall quality of the software.
* **Reduce the cost of software development and deployment:** DevOps can help organizations to reduce the cost of software development and deployment by automating manual tasks and by streamlining the software development and deployment process.

### Cloud Native Computing Foundation (CNCF)

The Cloud Native Computing Foundation (CNCF) is an open source software foundation that supports the development of cloud native technologies. The CNCF hosts a number of projects, including Kubernetes, Prometheus, and Jaeger.

The CNCF is important because it helps to promote the development and adoption of cloud native technologies. Cloud native technologies are designed to be scalable, reliable, and easy to deploy and manage in the cloud.

### Handling data privacy and compliance in the cloud

When handling data privacy and compliance in the cloud, it is important to:

* **Understand your data privacy and compliance requirements:** The first step is to understand your data privacy and compliance requirements. This includes understanding the laws and regulations that apply to your business and to your data.
* **Choose the right cloud provider:** Not all cloud providers are created equal. It is important to choose a cloud provider that has a strong track record of security and compliance.
* **Implement the necessary security and compliance controls:** Once you have chosen a cloud provider, you need to implement the necessary security and compliance controls. This includes implementing access control, data encryption, and data auditing.
* **Monitor your cloud environment:** It is important to monitor your cloud environment for security threats and compliance violations. This includes monitoring your cloud resources, your network traffic, and your security logs.

### Difference between cloud availability and reliability

Cloud availability refers to the percentage of time that a cloud service is up and running. Cloud reliability refers to the probability that a cloud service will perform as expected.

Availability is a measure of how often a system is available, while reliability is a measure of how well a system performs. A system can be available but not reliable, and vice versa.

For example, a cloud service may be available 99.99% of the time, but it may experience performance problems during peak usage times. This would mean that the service is available but not reliable.

### Containerization and container orchestration in the cloud

Containerization is a process of packaging up software code and all its dependencies so that it can run quickly and reliably from one computing environment to another. Containers are similar to virtual machines, but they are more lightweight and efficient.

Container orchestration is the process of managing and automating the deployment, scaling, and lifecycle of containers. Container orchestration tools such as Kubernetes allow you to run and manage containers at scale.

### Ensuring high availability in a cloud-based application

There are a number of ways to ensure high availability in a cloud-based application, including:

* **Using multiple availability zones:** Availability zones are isolated locations within a cloud region. By deploying your application across multiple availability zones, you can help to ensure that your application is still available even if there is an outage in one availability zone.
* **Using load balancing:** Load balancing distributes traffic across multiple instances of your application. This can help to improve the performance and availability of your application.
* **Using health checks:** Health checks monitor the health of your application instances. If a health check fails, the application instance is restarted or removed from the load balancer.
* **Using monitoring and alerting:** Monitoring and alerting tools can help you to identify and respond to problems with your application.

### Significance of cloud monitoring and management tools

Cloud monitoring and management tools are essential for managing cloud-based applications. These tools can help you to:

* **Monitor your cloud resources:** Cloud monitoring tools can help you to monitor the performance and health of your cloud resources. This includes monitoring your CPU usage, memory usage, and disk usage. On Amazon EC2, memory and disk space metrics are not published to CloudWatch by default and require the CloudWatch agent.
* **Manage your cloud resources:** Cloud management tools can help you to manage your cloud resources. This includes managing your cloud accounts, users, and permissions.
* **Automate cloud tasks:** Cloud automation tools can help you to automate cloud tasks, such as deploying new applications and scaling your applications up or down.

### How auto-scaling works in cloud environments

Auto-scaling is a feature that allows you to automatically scale your cloud resources up or down based on demand. Auto-scaling can help to improve the performance and cost-effectiveness of your cloud-based applications.

Auto-scaling works by monitoring the performance of your cloud resources and automatically scaling them up or down based on predefined rules. For example, you may configure auto-scaling to scale up your application instances when CPU usage exceeds a certain threshold.

Auto-scaling is a powerful tool that can help you to optimize your cloud-based applications for performance and cost-effectiveness.

### Cloud migration strategy and how to plan it

Cloud migration is the process of moving applications, data and other workloads from an on-premises environment, another cloud or another provider into a cloud environment, or between clouds. A cloud migration strategy is a plan for doing this. It should include a detailed assessment of your current environment, your goals for migrating to the cloud, and the steps you will take to achieve those goals.

To plan a cloud migration strategy, you should:

1. **Assess your current environment:** This includes understanding your current IT infrastructure, your applications, and your data.
2. **Define your goals:** What are you hoping to achieve by migrating to the cloud? Do you want to improve performance, reduce costs, or increase agility?
3. **Choose a cloud migration strategy:** Most migrations use one or more of the 7 Rs, as described in the [AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/large-migration-guide/migration-strategies.html). The best strategy for each application will depend on your specific goals and environment.
   * **Retire:** Turn off applications that are no longer needed instead of migrating them.
   * **Retain:** Keep applications where they are for now and revisit them later.
   * **Rehost (lift and shift):** Move applications and data to the cloud as they are, with no changes to the code or architecture.
   * **Relocate:** Move servers or clusters at the hypervisor level, such as moving a VMware environment to VMware Cloud on AWS, without new hardware or application changes.
   * **Repurchase (drop and shop):** Replace the application with a different product, often a SaaS platform.
   * **Replatform (lift, tinker and shift):** Make a few cloud optimizations, such as moving to a managed database, while the core architecture stays the same.
   * **Refactor (re-architect):** Rebuild the application to be cloud-native, often using microservices, serverless and managed services.
4. **Develop a migration plan:** Your migration plan should include a detailed timeline, budget, and risk assessment.
5. **Execute your migration plan:** Once you have developed your migration plan, you need to execute it carefully and monitor your progress.

### Role of load balancers in the cloud

Load balancers distribute traffic across multiple instances of an application. This can improve the performance and availability of the application.

Load balancers are typically used in the cloud to distribute traffic across multiple instances of a web application. However, they can also be used to distribute traffic across other types of applications, such as database servers and application servers.

### Managing cloud resources using automation

Automation can be used to manage cloud resources in a number of ways, such as:

* **Deploying new applications:** Automation can be used to deploy new applications to the cloud automatically. This can save time and reduce the risk of errors.
* **Scaling applications up or down:** Automation can be used to scale applications up or down based on demand. This can help to improve the performance and cost-effectiveness of applications.
* **Patching and updating applications:** Automation can be used to patch and update applications automatically. This can help to improve the security and reliability of applications.

### Multi-cloud and its advantages and challenges

Multi-cloud is the use of multiple cloud computing platforms. This can include public clouds, private clouds, and hybrid clouds.

### Advantages of multi-cloud:

* **Increased flexibility and choice:** Multi-cloud gives you the flexibility to choose the cloud platform that is best suited for your needs.
* **Improved redundancy and reliability:** Multi-cloud can help to improve the redundancy and reliability of your applications by distributing them across multiple cloud platforms.
* **Reduced costs:** Multi-cloud can help to reduce costs by allowing you to take advantage of different pricing models from different cloud providers.

### Challenges of multi-cloud:

* **Increased complexity:** Multi-cloud can increase the complexity of your IT environment. This can make it more difficult to manage and secure your applications.
* **Vendor lock-in:** It can be difficult to switch cloud providers once you have migrated your applications to the cloud. This is because cloud providers offer different features and services.
* **Security and compliance:** It can be difficult to ensure the security and compliance of your applications in a multi-cloud environment. This is because you need to comply with the security and compliance requirements of each cloud provider.

### Principles of microservices architecture in the cloud

Microservices architecture is a software design pattern that structures an application as a collection of loosely coupled services. Each service is self-contained and can be deployed and scaled independently.

Microservices architecture is well-suited for cloud computing because it allows applications to be scaled horizontally by adding more instances of each service. This can improve the performance and scalability of cloud-based applications.

### Cloud virtual private network (VPN)

A cloud virtual private network (VPN) is a secure tunnel between your on-premises network and the cloud. It allows you to access your cloud resources as if they were located on your on-premises network.

Cloud VPNs are typically used to connect on-premises networks to public clouds. However, they can also be used to connect on-premises networks to private clouds and hybrid clouds.

Cloud VPNs can be used to improve the security of traffic between your on-premises network and the cloud by encrypting it. A VPN does not reduce latency; it adds some overhead.

### How do you secure cloud-based applications and data?

There are a number of ways to secure cloud-based applications and data, including:

* **Access control:** Access control mechanisms such as identity and access management (IAM) and role-based access control (RBAC) can be used to control who has access to your cloud resources.
* **Data encryption:** Data encryption can be used to protect your data at rest and in transit.
* **Security monitoring:** Security monitoring tools can be used to monitor your cloud environment for security threats.
* **Security testing:** Security testing can be used to identify and fix security vulnerabilities in your cloud environment.

### Explain the concept of cloud networking and its components.

Cloud networking is the network infrastructure that is used to connect cloud resources to each other and to the internet. Cloud networking components include:

* **Virtual private networks (VPNs):** VPNs create a secure tunnel between your on-premises network and the cloud.
* **Load balancers:** Load balancers distribute traffic across multiple instances of an application.
* **Firewalls:** Firewalls protect your cloud resources from unauthorized access.
* **Routing:** Route tables direct traffic between subnets, gateways, and other networks. Providers abstract away physical routers and switches.

### What is cloud billing and cost management?

Cloud billing and cost management is the process of tracking and managing the costs of cloud computing. This includes understanding your cloud usage patterns, optimizing your cloud resources, and negotiating with cloud providers.

Cloud billing and cost management tools can help you to track your cloud usage and costs, identify areas where you can save money, and manage your cloud budget.

### How do you achieve data backup and recovery in the cloud?

There are a number of ways to achieve data backup and recovery in the cloud, including:

* **Snapshotting:** Snapshots are point-in-time copies of your cloud data. They can be used to restore your data to a previous state if it is lost or corrupted.
* **Replication:** Replication is the process of copying your cloud data to multiple locations. This can help to protect your data from data loss or corruption in one location.
* **Backup services:** Cloud providers offer a variety of backup services that can be used to back up your cloud data to an on-premises location or to another cloud provider.

### Describe the use of cloud-based databases.

Cloud-based databases are databases that are hosted and managed by a cloud provider. They offer a number of advantages over on-premises databases, such as:

* **Scalability:** Cloud-based databases are highly scalable, so you can easily scale them up or down to meet your changing needs.
* **Reliability:** Cloud-based databases are highly reliable, and cloud providers offer a variety of services to ensure the reliability of your databases.
* **Security:** Cloud-based databases are secure, and cloud providers offer a variety of security services to protect your data.

### What are serverless functions, and when do you use them?

Serverless functions are a type of cloud computing service that allows you to run code without having to provision or manage servers. Serverless functions are typically used to run event-driven workloads, such as processing payments or sending notifications. Common examples are AWS Lambda, Azure Functions, and Cloud Run functions (formerly Cloud Functions) in Google Cloud.

Serverless functions are a good choice for workloads that are unpredictable or that need to be scaled up or down quickly. They are also a good choice for workloads that are infrequently accessed, as you only pay for the time that your functions are running.

Here are some examples of when you might use serverless functions:

* Processing payments
* Sending notifications
* Resizing images
* Transcoding videos
* Analyzing data

Serverless functions can be a powerful tool for developing and deploying cloud-based applications. However, it is important to choose the right cloud provider and to design your applications in a way that takes advantage of the benefits of serverless functions.

### Role of Identity and Access Management (IAM) in the cloud

Identity and Access Management (IAM) is a set of policies and procedures that control who has access to cloud resources and what they can do with those resources. IAM is important in the cloud because it helps to protect cloud resources from unauthorized access and use.

IAM typically includes the following components:

* **Authentication:** Authentication is the process of verifying that a user is who they say they are.
* **Authorization:** Authorization is the process of determining what a user is allowed to do with cloud resources.
* **Auditing:** Auditing is the process of tracking user activity in the cloud.

### Cloud application programming interface (API)

A cloud application programming interface (API) is a set of rules that define how applications can interact with each other. Cloud APIs are used to develop cloud-based applications and to integrate cloud-based applications with on-premises applications.

### How to troubleshoot cloud-based applications

There are a number of ways to troubleshoot cloud-based applications, including:

* **Monitoring:** Monitoring your cloud-based applications can help you to identify and troubleshoot problems early on.
* **Logging:** Logging can help you to track down the root cause of problems with your cloud-based applications.
* **Debugging:** Debugging can help you to identify and fix specific problems with your cloud-based applications.
* **Support:** Cloud providers offer a variety of support options to help you troubleshoot problems with your cloud-based applications.

### How to handle data migration in the cloud

There are a number of ways to handle data migration in the cloud, including:

* **Rehost (lift and shift):** Move data and the applications that use it as they are, with no changes to the data structure or code. Online tools such as AWS DataSync (files and objects) or AWS Database Migration Service (databases) can copy the data over the network, and offline transfer is an option when the data set is too large to move over the network in a reasonable time. AWS Snow Family devices reach end of support on December 31, 2026, so check current options first.
* **Replatform (lift, tinker and shift):** Make a few changes, such as moving a self-managed database to a managed database service, while the core data model and architecture stay the same.
* **Refactor (re-architect):** Redesign the data store and the application to take full advantage of cloud-native capabilities, such as managed services, microservices and serverless architectures.

These are the three strategies that move data most often. The full list of 7 Rs (also Retire, Retain, Relocate and Repurchase) is in [Cloud migration strategy and how to plan it](#cloud-migration-strategy-and-how-to-plan-it). The best data migration strategy for you will depend on your specific needs and environment.

### Role of a reverse proxy in a cloud environment

A reverse proxy is a server that sits in front of one or more web servers and forwards requests to them. Reverse proxies can be used to improve the performance, security, and scalability of web applications.

In a cloud environment, reverse proxies can be used to:

* Distribute traffic across multiple web servers. This can improve the performance of web applications by reducing latency and increasing throughput.
* Load balance traffic between web servers. This can help to ensure that web applications are available even if one web server fails.
* Terminate SSL/TLS connections. This can reduce the workload on web servers and improve security.
* Cache static content. This can improve the performance of web applications by reducing bandwidth usage and latency.

### Principles of cloud data warehousing

Cloud data warehousing is the use of cloud computing to build and manage data warehouses. Managed options include Amazon Redshift, Google BigQuery, and Azure Synapse Analytics. Many of these services scale compute and storage independently, and they are billed by compute time, storage, or data scanned, depending on the product.

### Cloud bursting and when it is useful

Cloud bursting is a technique for scaling your on-premises applications to the cloud. This can be useful when your on-premises infrastructure cannot handle spikes in traffic or workloads.

Cloud bursting can be used to:

* Scale up your on-premises applications to meet unexpected spikes in traffic or workloads.
* Run batch jobs or other computationally intensive tasks in the cloud.
* Develop and test new applications in the cloud.

### How to monitor and manage cloud resource performance

There are a number of ways to monitor and manage cloud resource performance, including:

* **Monitoring:** Monitoring your cloud resources can help you to identify and troubleshoot performance problems early on.
* **Logging:** Logging can help you to track down the root cause of performance problems with your cloud resources.
* **Alerting:** Alerting can help you to be notified of performance problems with your cloud resources so that you can take corrective action.
* **Optimization:** Optimization can help you to improve the performance of your cloud resources by making changes to your configuration or code.

### Role of a Content Delivery Network (CDN)

A Content Delivery Network (CDN) is a network of servers that deliver content to users based on their geographic location. CDNs can be used to improve the performance, reliability, and security of cloud content delivery.

In a cloud environment, CDNs can be used to:

* Deliver content to users from servers that are located close to them. This can reduce latency and improve the performance of cloud-based applications.
* Improve the reliability of cloud-based applications by distributing content across multiple servers.
* Protect cloud-based applications from DDoS attacks by caching content on CDN servers.

### Use of containers in cloud computing

Containers are a lightweight virtualization technology that can be used to package and deploy applications. Containers are well-suited for cloud computing because they allow applications to be scaled and deployed quickly and easily.

Containers can be used in cloud computing to:

* Deploy applications to multiple cloud providers.
* Scale applications up or down quickly and easily.
* Start faster and use less overhead than VMs, because containers share the host operating system kernel.
* Reduce the cost of running applications by reducing the number of servers that are needed.

### How to ensure data encryption in the cloud

There are a number of ways to ensure data encryption in the cloud, including:

* **Client-side encryption:** Client-side encryption encrypts data before it is uploaded to the cloud. This gives you more control over your data encryption keys.
* **Server-side encryption:** The provider encrypts data at rest after it is received. Major object storage services enable this by default.
* **Transit encryption:** Transit encryption encrypts data while it is being transmitted between your on-premises environment and the cloud.

### Cloud Security Alliance (CSA)

The Cloud Security Alliance (CSA) is a non-profit organization that promotes best practices for cloud security. The CSA offers a number of resources, including the Cloud Controls Matrix (CCM), which is a framework for assessing and managing cloud security risks.

### Principles of disaster recovery in the cloud

Disaster recovery in the cloud is the process of restoring your cloud-based applications and data after a disaster. Disaster recovery planning should include the following:

* **Risk assessment:** Identify the risks to your cloud-based applications and data.
* **Recovery strategy:** Develop a plan for recovering your cloud-based applications and data after a disaster.
* **Testing:** Test your disaster recovery plan regularly to ensure that it works.

### How to choose the right cloud service model for a project

There are three main cloud service models:

* **Infrastructure as a Service (IaaS):** IaaS provides you with access to computing resources, such as servers, storage, and networking.
* **Platform as a Service (PaaS):** PaaS provides you with a platform for developing and deploying applications.
* **Software as a Service (SaaS):** SaaS provides you with access to software applications that are hosted in the cloud.

The best cloud service model for your project will depend on your specific needs and requirements.

### Cloud application architecture pattern

A cloud application architecture pattern is a blueprint for designing and building cloud-based applications. There are a number of different cloud application architecture patterns, including:

* **Microservices architecture:** Microservices architecture is a software design pattern that structures an application as a collection of loosely coupled services.
* **Serverless architecture:** Serverless architecture is a cloud computing model in which the cloud provider automatically manages the server infrastructure.
* **Containerized architecture:** Containerized architecture is a software development and deployment approach in which applications are packaged into containers.

### Use of serverless databases in the cloud

Serverless databases are databases that are managed by a cloud provider. Serverless databases offer a number of advantages over traditional managed databases, such as:

* **Scalability:** Serverless databases are highly scalable, so you can easily scale them up or down to meet your changing needs.
* **Cost savings:** Serverless databases can help you to save money on database costs, as you only pay for the resources that you use.
* **Ease of use:** Serverless databases are easy to use, so you can focus on developing your applications without having to worry about managing databases.

Here are some examples of serverless databases:

* Amazon Aurora Serverless v2
* Google Cloud Firestore
* Microsoft Azure Cosmos DB

Serverless databases can be a good choice for a variety of workloads, such as:

* Web applications
* Mobile applications
* IoT applications
* Real-time data processing applications

### How to implement high availability in a cloud infrastructure

High availability in a cloud infrastructure refers to the ability of a system to remain up and running despite the failure of some of its components. This can be achieved through a number of ways, including:

* **Redundancy:** Deploying redundant components, such as load balancers, servers, and storage devices, can help to ensure that the system remains available even if one component fails.
* **Geographic distribution:** Deploying components across multiple geographic regions can help to protect the system from outages caused by regional disasters.
* **Automated failover:** Implementing automated failover mechanisms can help to ensure that traffic is automatically routed to healthy components in the event of a failure.

### Role of cloud identity and access management

Cloud identity and access management (IAM) is the process of managing who has access to cloud resources and what they can do with those resources. IAM is important for cloud security because it helps to protect cloud resources from unauthorized access and use.

Cloud IAM typically includes the following components:

* **Authentication:** Authentication is the process of verifying that a user is who they say they are.
* **Authorization:** Authorization is the process of determining what a user is allowed to do with cloud resources.
* **Auditing:** Auditing is the process of tracking user activity in the cloud.

### Continuous integration and continuous deployment (CI/CD) in the cloud

Continuous integration and continuous delivery or deployment (CI/CD) is a software development practice that automates the building, testing, and deployment of software. CI/CD can help to improve the quality and reliability of software, and it can also help to shorten the time it takes to release new software features.

CI/CD is well-suited for cloud computing because cloud platforms offer a variety of services that can be used to automate the CI/CD process. For example, cloud providers offer services for building, testing, and deploying code, as well as services for managing infrastructure and monitoring applications.

### How to achieve data replication in the cloud

Data replication in the cloud is the process of copying data to multiple locations. This can be done to improve performance, reliability, and disaster recovery.

There are a number of ways to achieve data replication in the cloud, including:

* **Database replication:** Database replication tools can be used to replicate data between databases.
* **Object storage replication:** Object storage providers offer replication features that can be used to replicate data between object storage buckets.
* **File storage replication:** File storage providers offer replication features that can be used to replicate data between file storage buckets.

### Cloud DNS service and how it works

A cloud DNS service is a DNS service that is hosted in the cloud. Cloud DNS services offer a number of advantages over traditional on-premises DNS services, such as:

* **Scalability:** Cloud DNS services are highly scalable, so you can easily scale them up or down to meet your changing needs.
* **Reliability:** Managed DNS services run on globally distributed name servers, which reduces the impact of individual server failures.
* **Security:** Some managed DNS services support DNSSEC, which lets resolvers verify that DNS responses are authentic.

A cloud DNS service hosts the records for your domains (such as A, AAAA, and CNAME records) and answers queries for them from a globally distributed network of name servers. Examples include Amazon Route 53, Google Cloud DNS, and Azure DNS.

### Benefits of cloud serverless compute platforms

Cloud serverless compute platforms are platforms that allow you to run code without having to provision or manage servers. Cloud serverless compute platforms offer a number of advantages over traditional server-based platforms, such as:

* **Scalability:** Cloud serverless compute platforms are highly scalable, so you can easily scale your applications up or down to meet your changing needs.
* **Cost savings:** Cloud serverless compute platforms can help you to save money on server costs, as you only pay for the resources that you use.
* **Ease of use:** Cloud serverless compute platforms are easy to use, so you can focus on developing your applications without having to worry about managing servers.

Here are some examples of cloud serverless compute platforms:

* AWS Lambda
* Google Cloud Functions (now Cloud Run functions)
* Microsoft Azure Functions

Cloud serverless compute platforms can be a good choice for a variety of workloads, such as:

* Web applications
* Mobile applications
* IoT applications
* Event-driven applications

### How to handle cloud storage security and access control

Cloud storage security and access control is important to protect your data from unauthorized access, use, disclosure, disruption, modification, or destruction. Here are some tips for handling cloud storage security and access control:

* **Use encryption:** Encrypt your data at rest and in transit to protect it from unauthorized access.
* **Implement access control:** Use access control lists (ACLs) or role-based access control (RBAC) to control who has access to your data and what they can do with it.
* **Enable auditing:** Enable auditing to track who accesses your data and what actions they take.
* **Monitor your cloud storage:** Monitor your cloud storage for suspicious activity.

### Cloud architecture diagram and its importance

A cloud architecture diagram is a visual representation of the components of a cloud architecture and how they are interconnected. Cloud architecture diagrams are important because they can help you to:

* Understand the different components of a cloud architecture.
* Identify potential bottlenecks and security risks.
* Plan for future growth and scalability.

### Principles of cloud compliance and auditing

Cloud compliance is the process of ensuring that your cloud environment meets all applicable regulations. Cloud auditing is the process of collecting and analyzing evidence to determine whether cloud resources are being used in accordance with cloud compliance requirements.

Here are some principles of cloud compliance and auditing:

* **Identify your compliance requirements:** Identify the regulations that apply to your cloud environment.
* **Assess your cloud environment:** Assess your cloud environment to identify potential compliance gaps.
* **Implement controls:** Implement controls to address any compliance gaps.
* **Monitor your cloud environment:** Monitor your cloud environment for compliance violations.

### How to design a resilient cloud architecture

A resilient cloud architecture is an architecture that can withstand and recover from failures. Here are some tips for designing a resilient cloud architecture:

* **Use redundancy:** Deploy redundant components, such as load balancers, servers, and storage devices, to ensure that your architecture remains available even if one component fails.
* **Use geographic distribution:** Deploy components across multiple geographic regions to protect your architecture from regional disasters.
* **Use automation:** Automate failover and recovery mechanisms to ensure that your architecture can recover quickly from failures.

### Cloud cost optimization and how to achieve it

Cloud cost optimization is the process of reducing your cloud costs without sacrificing performance or reliability. Here are some tips for achieving cloud cost optimization:

* **Right-size your resources:** Choose the right cloud resources for your needs and avoid overprovisioning.
* **Use reserved instances:** Reserved instances and savings plans can offer significant discounts for steady, predictable workloads.
* **Use spot instances:** Spot instances can offer even greater discounts on cloud resources, but the provider can reclaim them at short notice, so use them only for interruptible workloads.
* **Monitor your cloud usage:** Monitor your cloud usage to identify areas where you can reduce costs.

### Use of cloud-native application development

Cloud-native application development is a software development approach that is designed to build and run applications in the cloud. Cloud-native applications are typically built using microservices and containerization.

Here are some of the benefits of cloud-native application development:

* **Scalability:** Cloud-native applications are highly scalable and can be easily scaled up or down to meet your changing needs.
* **Agility:** Cloud-native applications can be developed and deployed quickly and easily.
* **Resilience:** Well-designed cloud-native applications tolerate failures of individual components more gracefully.
* **Cost savings:** Cloud-native applications can help you to save money on cloud costs.

Cloud-native application development can be a good choice for a variety of workloads, such as:

* Web applications
* Mobile applications
* IoT applications
* Real-time data processing applications

### How to manage cloud resources using Infrastructure as Code (IaC)

Infrastructure as Code (IaC) is a practice of managing and provisioning cloud infrastructure using code. IaC can help you to:

* Automate the provisioning and configuration of cloud resources.
* Reduce manual errors.
* Improve consistency and repeatability.
* Facilitate collaboration.

There are a number of different IaC tools available, such as Terraform, AWS CloudFormation, and Azure Resource Manager (ARM) templates or Bicep.

To manage cloud resources using IaC, you can follow these steps:

1. Define your infrastructure in code using an IaC tool.
2. Review the planned changes (for example, with `terraform plan`), then apply the code to your cloud provider.
3. Monitor your infrastructure for changes and apply updates as needed.

### Cloud-native container orchestration platform

A cloud-native container orchestration platform is a platform that helps you to manage and automate the deployment, scaling, and monitoring of containerized applications. Cloud-native container orchestration platforms typically offer features such as:

* Container scheduling and orchestration
* Service discovery and load balancing
* Automatic scaling
* Health monitoring and self-healing
* Storage and networking management

Some popular cloud-native container orchestration platforms include:

* Kubernetes
* Docker Swarm
* Amazon Elastic Kubernetes Service (EKS)
* Google Kubernetes Engine (GKE)
* Azure Kubernetes Service (AKS)

### Principles of cloud application performance tuning

Cloud application performance tuning is the process of optimizing the performance of cloud-based applications. Cloud application performance tuning can involve a variety of activities, such as:

* Identifying performance bottlenecks
* Optimizing code and database queries
* Configuring cloud resources for optimal performance
* Using caching and load balancing
* Monitoring application performance and making adjustments as needed

### How to achieve data governance in the cloud

Data governance is the process of managing data to ensure that it is accurate, complete, consistent, secure, and accessible. Data governance is important in the cloud because it can help you to:

* Protect your data from unauthorized access, use, disclosure, disruption, modification, or destruction.
* Ensure that your data is compliant with all applicable regulations.
* Improve the quality and reliability of your data.

Here are some tips for achieving data governance in the cloud:

* Develop a data governance policy that defines your data governance requirements.
* Implement data access controls to control who has access to your data and what they can do with it.
* Encrypt your data at rest and in transit.
* Monitor your data for suspicious activity.
* Audit your data regularly to ensure compliance with your data governance policy.

### Role of cloud access control policies

Cloud access control policies define who has access to cloud resources and what they can do with those resources. Cloud access control policies are important for cloud security because they can help to protect cloud resources from unauthorized access and use.

In practice, access control policies are expressed as IAM policies in AWS, role assignments in Azure role-based access control (RBAC), and IAM policy bindings in Google Cloud. Authentication, authorization, and auditing are covered in the IAM section above.

### Use of cloud-based message queues

Cloud-based message queues are a way to decouple applications and services. Message queues allow applications to send and receive messages asynchronously. This can improve the performance, scalability, and reliability of applications.

Some popular cloud-based messaging services include:

* Amazon Simple Queue Service (SQS)
* Google Cloud Pub/Sub
* Azure Service Bus

Cloud-based message queues can be used for a variety of tasks, such as:

* Decoupling applications and services
* Implementing event-driven architectures
* Processing large volumes of data
* Building scalable and reliable applications

### How to design a cloud data warehouse

When designing a cloud data warehouse, you need to consider the following factors:

* **Data sources:** What data sources will your data warehouse be ingesting?
* **Data volumes:** How much data will your data warehouse be storing and processing?
* **User requirements:** What are the analytical and reporting needs of your users?
* **Budget:** How much can you afford to spend on your data warehouse?

Once you have considered these factors, you can start to design your data warehouse architecture. Here are some key components of a cloud data warehouse architecture:

* **Data ingestion:** The data ingestion layer is responsible for ingesting data from your data sources and loading it into your data warehouse.
* **Data storage:** The data storage layer is responsible for storing your data in a scalable and efficient manner.
* **Data processing:** The data processing layer is responsible for transforming and processing your data to make it ready for analysis.
* **Query layer:** The query layer is responsible for providing users with access to your data for analysis and reporting.

### Cloud backup and recovery strategy

A cloud backup and recovery strategy is a plan for protecting your data in the cloud from loss or corruption. A cloud backup and recovery strategy should include the following components:

* **Regular backups:** You should regularly back up your data to the cloud.
* **Offsite storage:** You should store your backups in an offsite location to protect them from physical disasters.
* **Testing:** You should regularly test your backup and recovery procedures to ensure that they work as expected.

### Principles of cloud load balancing

Cloud load balancing is the process of distributing traffic across multiple servers or cloud instances. Cloud load balancing can improve the performance, scalability, and reliability of applications.

There are a number of different cloud load balancing algorithms, such as:

* **Round robin:** Round robin load balancing distributes traffic evenly across all servers or cloud instances.
* **Weighted round robin:** Weighted round robin load balancing distributes traffic across servers or cloud instances based on their weight.
* **Least connections:** Least connections load balancing distributes traffic to the server or cloud instance with the fewest active connections.
* **Least response time:** Least response time load balancing distributes traffic to the server or cloud instance with the fastest response time.

### How to secure data transfer in a cloud environment

There are a number of ways to secure data transfer in a cloud environment, including:

* **Encryption:** Encrypting your data at rest and in transit can protect it from unauthorized access.
* **VPN:** Using a VPN can create a secure tunnel between your on-premises network and the cloud.
* **IAM:** Using IAM can control who has access to your data and what they can do with it.

### Cloud disaster recovery planning

Cloud disaster recovery planning is the process of developing a plan to recover your data and applications in the event of a disaster. A cloud disaster recovery plan should include the following components:

* **Risk assessment:** Identify the risks to your data and applications.
* **Recovery strategy:** Develop a plan to recover your data and applications in the event of a disaster.
* **Testing:** Regularly test your disaster recovery plan to ensure that it works as expected.

### Use of cloud API gateways

Cloud API gateways are a way to manage and secure API access. Cloud API gateways can help you to:

* Enforce authentication, rate limiting, and other access controls for your APIs.
* Provide a single point of entry for your APIs.

Some popular cloud API gateways include:

* Amazon API Gateway
* Google Cloud API Gateway
* Azure API Management

Cloud API gateways can be used for a variety of purposes, such as:

* Exposing internal APIs to external users.
* Providing a single point of entry for a microservices architecture.
* Implementing a serverless architecture.

### How to achieve cloud network segmentation

Cloud network segmentation is the process of dividing a cloud network into smaller, isolated subnets. This can help to improve security, performance, and manageability.

There are a number of ways to achieve cloud network segmentation, including:

* **Virtual networks:** Isolated networks you create within your cloud provider's environment. They are called VPCs in AWS and Google Cloud, and virtual networks (VNets) in Azure.
* **Subnets:** Subnets are divisions of a VPC that you can use to further isolate your network.
* **Security groups:** Stateful firewall rules attached to instances or network interfaces (AWS). Azure uses network security groups (NSGs) for similar filtering.
* **Network ACLs:** Stateless allow and deny rules applied at the subnet boundary (AWS).

### Role of a cloud management console

A cloud management console is a web-based tool that you can use to manage your cloud resources. Cloud management consoles typically offer features such as:

* **Resource provisioning and management:** You can use a cloud management console to provision and manage your cloud resources, such as servers, storage, and networking.
* **Monitoring and alerting:** You can use a cloud management console to monitor your cloud resources for health and performance.
* **Cost management:** You can use a cloud management console to track your cloud costs and usage.

### Principles of cloud data archiving

Cloud data archiving is the process of storing data in the cloud for long-term retention. Cloud data archiving can be used to comply with regulations, preserve historical data, and reduce storage costs.

Here are some principles of cloud data archiving:

* **Choose the right storage class:** Cloud providers offer a variety of storage classes that are designed for different needs. When choosing a storage class for your archived data, consider the following factors: access frequency, cost, and durability.
* **Implement a retention policy:** A retention policy defines how long data will be stored before it is deleted. Implementing a retention policy can help to reduce storage costs and improve compliance.
* **Use a data archiving tool:** A data archiving tool can help you to automate the process of archiving data to the cloud.

### How to manage cloud-based databases

There are a number of ways to manage cloud-based databases, including:

* **Use a database management system (DBMS):** A DBMS is a software application that you can use to manage and administer databases. DBMSs typically offer features such as schema creation, data manipulation, and performance monitoring.
* **Use a cloud-based database service:** Cloud providers offer a variety of cloud-based database services, such as relational databases, NoSQL databases, and managed database services. Cloud-based database services can make it easier to manage your databases by eliminating the need to provision and manage hardware and software.

### Cloud-native service mesh

A cloud-native service mesh is a network of infrastructure that provides communication, load balancing, and other functions for microservices. Service meshes can help to improve the performance, reliability, and security of microservices architectures.

Some popular cloud-native service meshes include:

* Istio
* Linkerd
* HashiCorp Consul

### Use of cloud resource tagging

Cloud resource tagging is the process of adding metadata to cloud resources. Cloud resource tags can be used to organize, filter, and track cloud resources.

Here are some examples of how you can use cloud resource tags:

* **Organize your cloud resources:** You can use tags to organize your cloud resources by project, environment, or application.
* **Filter your cloud resources:** You can use tags to filter your cloud resources when viewing them in the cloud management console. This can make it easier to find the resources that you are looking for.
* **Track your cloud resources:** You can use tags to track your cloud resources over time. This can help you to identify unused resources and optimize your cloud costs.

### How to design a cloud content delivery strategy

To design a cloud content delivery strategy, you need to consider the following factors:

* **Content:** What type of content will you be delivering?
* **Audience:** Who is your target audience?
* **Location:** Where is your audience located?
* **Performance:** What level of performance do you need to achieve?
* **Cost:** How much are you willing to spend on content delivery?

Once you have considered these factors, you can start to design your cloud content delivery strategy. Here are some key components of a cloud content delivery strategy:

* **Content delivery network (CDN):** A CDN is a network of servers that are distributed around the world. Examples include Amazon CloudFront, Azure Front Door, and Google Cloud CDN. CDNs can be used to deliver content to users quickly and reliably.
* **Content caching:** Content caching can be used to store content closer to users, which can improve performance.
* **Content optimization:** Content optimization can be used to reduce the size of content, which can improve performance and reduce bandwidth costs.

### Cloud governance and policy enforcement

Cloud governance is the process of managing and controlling cloud resources. Cloud policy enforcement is the process of ensuring that cloud resources are used in accordance with cloud governance policies.

Cloud governance policies typically include the following:

* **Access control:** Who has access to cloud resources and what they can do with them.
* **Resource usage:** How cloud resources can be used.
* **Security:** How cloud resources should be protected.

Cloud policy enforcement can be implemented using a variety of tools and technologies, such as cloud identity and access management (IAM) tools and cloud security tools.

### Principles of cloud application scaling

Cloud application scaling is the process of adjusting the resources allocated to a cloud application to meet demand. Cloud application scaling can be done manually or automatically.

There are two main types of cloud application scaling:

* **Horizontal scaling:** Horizontal scaling involves adding or removing servers from a cloud application.
* **Vertical scaling:** Vertical scaling involves adding or removing resources to a server, such as CPU, memory, and storage.

### How to achieve compliance in a multi-cloud environment

To achieve compliance in a multi-cloud environment, you need to:

1. **Identify your compliance requirements:** Identify the regulations that apply to your organization.
2. **Assess your multi-cloud environment:** Assess your multi-cloud environment to identify any compliance gaps.
3. **Implement controls:** Implement controls to address any compliance gaps.
4. **Monitor your multi-cloud environment:** Monitor your multi-cloud environment for compliance violations.

### Role of cloud encryption at rest and in transit

Cloud encryption at rest and in transit is used to protect cloud data from unauthorized access, use, disclosure, disruption, modification, or destruction.

* **Cloud encryption at rest:** Cloud encryption at rest encrypts data when it is stored on cloud storage devices.
* **Cloud encryption in transit:** Cloud encryption in transit encrypts data when it is being transmitted between cloud resources or between your on-premises network and the cloud.

### Use of cloud-based data lakes

Cloud-based data lakes are a type of cloud storage that is designed to store large amounts of raw data. Cloud-based data lakes can be used for a variety of purposes, such as data analytics, machine learning, and artificial intelligence.

Here are some of the benefits of using cloud-based data lakes:

* **Scalability:** Cloud-based data lakes are highly scalable, so you can easily add or remove storage capacity as needed.
* **Cost-effectiveness:** Cloud-based data lakes can be more cost-effective than traditional on-premises data warehouses.
* **Ease of use:** Cloud-based data lakes are typically easy to use and manage.

### Cloud resource lifecycle management

Cloud resource lifecycle management is the process of managing cloud resources throughout their lifecycle, from creation to deletion. This includes provisioning, configuring, monitoring, optimizing, and decommissioning cloud resources.

Here are some of the key benefits of cloud resource lifecycle management:

* **Improved efficiency and cost savings:** Cloud resource lifecycle management can help you to automate and streamline your cloud resource management processes, which can lead to improved efficiency and cost savings.
* **Reduced risk:** Cloud resource lifecycle management can help you to reduce the risk of human error and improve the compliance of your cloud environment.
* **Increased agility and scalability:** Cloud resource lifecycle management can help you to quickly and easily provision and scale your cloud resources to meet changing demand.

### Cloud security incident response plan

A cloud security incident response plan is a plan for responding to a security incident in the cloud. The plan should include the following components:

* **Incident detection:** How will you detect security incidents in your cloud environment?
* **Incident response:** What steps will you take to respond to a security incident?
* **Incident recovery:** How will you recover your cloud environment from a security incident?

### Principles of cloud application monitoring

Cloud application monitoring is the process of collecting and analyzing data about the performance and health of cloud applications. Cloud application monitoring can help you to:

* **Identify and resolve performance issues:** Cloud application monitoring can help you to identify and resolve performance issues in your cloud applications before they impact your users.
* **Improve the reliability of your cloud applications:** Cloud application monitoring can help you to improve the reliability of your cloud applications by detecting and resolving potential problems before they cause outages.
* **Reduce costs:** Cloud application monitoring can help you to reduce costs by identifying and eliminating unused resources.

### How to ensure data privacy in the cloud

There are a number of ways to ensure data privacy in the cloud, including:

* **Encrypt your data:** Encrypting your data at rest and in transit can protect it from unauthorized access.
* **Use access control:** Use access control to control who has access to your data and what they can do with it.
* **Audit your data:** Audit your data to track who accesses it and when.
* **Use a cloud security information and event management (SIEM) tool:** A cloud SIEM tool can help you to detect and respond to security threats to your cloud data.

### Cloud network optimization

Cloud network optimization is the process of optimizing your cloud network to improve performance, reliability, and security. Cloud network optimization can involve a variety of activities, such as:

* **Choosing the right network architecture:** Choosing the right network architecture for your cloud environment is essential for optimizing performance and reliability.
* **Configuring your cloud network:** Configuring your cloud network correctly is important for optimizing performance, security, and cost.
* **Monitoring your cloud network:** Monitoring your cloud network for performance issues and security threats is essential for maintaining an optimized cloud network.

### Use of cloud-based container registries

Cloud-based container registries are repositories for storing and distributing container images. Container registries make it easy to share container images with other developers and to deploy containerized applications to production environments.

Managed registries include Amazon Elastic Container Registry (ECR), Azure Container Registry (ACR), and Google Artifact Registry. Google Container Registry (gcr.io) has been retired and replaced by Artifact Registry, so new work should use Artifact Registry.

### Cloud access management strategy

A cloud access management strategy is a plan for managing who has access to cloud resources and what they can do with those resources. A cloud access management strategy should include the following components:

* **Identity and access management (IAM):** IAM is the process of managing who has access to cloud resources and what they can do with those resources.
* **Authorization:** Authorization is the process of determining what a user is allowed to do with cloud resources.
* **Authentication:** Authentication is the process of verifying that a user is who they say they are.

### Cloud disaster recovery testing plan

A cloud disaster recovery testing plan is a plan for testing your cloud disaster recovery procedures. The plan should include the following components:

* **Test schedule:** How often will you test your cloud disaster recovery procedures?
* **Test scenarios:** What cloud disaster recovery scenarios will you test?
* **Test procedures:** What steps will you take to test your cloud disaster recovery procedures?
* **Test results:** How will you record and analyze the results of your cloud disaster recovery tests?

### Principles of cloud application logging

Cloud application logging is the process of collecting and storing logs from cloud applications. Cloud application logging can help you to:

* **Monitor the performance and health of your cloud applications:** Cloud application logs can be used to monitor the performance and health of your cloud applications.
* **Troubleshoot problems with your cloud applications:** Cloud application logs can be used to troubleshoot problems with your cloud applications.
* **Audit the use of your cloud applications:** Cloud application logs can be used to audit the use of your cloud applications.

### How to achieve cost transparency in the cloud

To achieve cost transparency in the cloud, you need to:

* **Track your cloud costs:** Track your cloud costs to identify areas where you can save money.
* **Analyze your cloud usage:** Analyze your cloud usage to identify unused resources.
* **Forecast your cloud costs:** Forecast your cloud costs to ensure that you are not overspending.
* **Use cloud cost optimization tools:** Use cloud cost optimization tools to help you to optimize your cloud costs.

### Role of cloud compliance reporting

Cloud compliance reporting is the process of generating reports on the compliance of your cloud environment with applicable regulations. Cloud compliance reporting can help you to:

* **Demonstrate compliance to auditors:** Cloud compliance reports can be used to demonstrate compliance to auditors.
* **Identify compliance gaps:** Cloud compliance reports can be used to identify compliance gaps in your cloud environment.
* **Remediate compliance gaps:** Cloud compliance reports can be used to remediate compliance gaps in your cloud environment.

## Amazon Web Services (AWS)

 1. [What is AWS and how does it work?](#what-is-aws-and-how-does-it-work)
 2. [Explain the difference between EC2 and Lambda.](#explain-the-difference-between-ec2-and-lambda)
 3. [What is the AWS Well-Architected Framework?](#what-is-the-aws-well-architected-framework)
 4. [Describe AWS IAM (Identity and Access Management).](#describe-aws-iam-identity-and-access-management)
 5. [What is the difference between Amazon RDS and Amazon DynamoDB?](#what-is-the-difference-between-amazon-rds-and-amazon-dynamodb)
 6. [What are Amazon VPC and subnet?](#what-are-amazon-vpc-and-subnet)
 7. [What is the significance of an AWS Availability Zone?](#what-is-the-significance-of-an-aws-availability-zone)
 8. [What is an S3 bucket?](#what-is-an-s3-bucket)
 9. [What is Amazon CloudWatch, and how is it used?](#what-is-amazon-cloudwatch-and-how-is-it-used)
 10. [Define the term "Elastic Load Balancing" in AWS.](#define-the-term-elastic-load-balancing-in-aws)
 11. [What is AWS Elastic Beanstalk, and how does it work?](#what-is-aws-elastic-beanstalk-and-how-does-it-work)
 12. [Describe the use cases for Amazon SNS and Amazon SQS.](#describe-the-use-cases-for-amazon-sns-and-amazon-sqs)
 13. [How does AWS Lambda handle concurrent executions?](#how-does-aws-lambda-handle-concurrent-executions)
 14. [What are AWS CloudFormation templates, and how do they work?](#what-are-aws-cloudformation-templates-and-how-do-they-work)
 15. [Explain the differences between Amazon S3, EBS, and EFS.](#explain-the-differences-between-amazon-s3-ebs-and-efs)
 16. [How do you secure your AWS resources using Security Groups and NACLs?](#how-do-you-secure-your-aws-resources-using-security-groups-and-nacls)
 17. [What is Amazon Aurora, and how does it differ from other databases?](#what-is-amazon-aurora-and-how-does-it-differ-from-other-databases)
 18. [Describe the AWS Global Accelerator service.](#describe-the-aws-global-accelerator-service)
 19. [What is the AWS Trusted Advisor?](#what-is-the-aws-trusted-advisor)
 20. [How does AWS handle data encryption at rest and in transit?](#how-does-aws-handle-data-encryption-at-rest-and-in-transit)
 21. [Explain the significance of Amazon Route 53.](#explain-the-significance-of-amazon-route-53)
 22. [What is Amazon ElastiCache, and how does it improve application performance?](#what-is-amazon-elasticache-and-how-does-it-improve-application-performance)
 23. [How do you scale an application on AWS?](#how-do-you-scale-an-application-on-aws)
 24. [What is the AWS Serverless Application Model (SAM)?](#what-is-the-aws-serverless-application-model-sam)
 25. [Explain AWS Elastic Container Service (ECS) and Kubernetes.](#explain-aws-elastic-container-service-ecs-and-kubernetes)
 26. [Describe the features of Amazon Redshift.](#describe-the-features-of-amazon-redshift)
 27. [How does AWS Step Functions work, and what are its use cases?](#how-does-aws-step-functions-work-and-what-are-its-use-cases)
 28. [What is AWS Lambda Layers?](#what-is-aws-lambda-layers)
 29. [How do you migrate an on-premises database to AWS?](#how-do-you-migrate-an-on-premises-database-to-aws)
 30. [Explain the use of AWS Direct Connect.](#explain-the-use-of-aws-direct-connect)
 31. [What is AWS Elastic File System (EFS)?](#what-is-aws-elastic-file-system-efs)
 32. [Describe the benefits of using AWS CloudTrail.](#describe-the-benefits-of-using-aws-cloudtrail)
 33. [What are the types of Elastic Load Balancing?](#what-are-the-types-of-elastic-load-balancing)
 34. [How do you optimize costs in AWS?](#how-do-you-optimize-costs-in-aws)
 35. [What are AWS Organizations, and how are they used?](#what-are-aws-organizations-and-how-are-they-used)
 36. [Explain the benefits of using AWS Fargate.](#explain-the-benefits-of-using-aws-fargate)
 37. [How do you monitor AWS resources using CloudWatch Alarms?](#how-do-you-monitor-aws-resources-using-cloudwatch-alarms)
 38. [AWS Snowball service and when is it used?](#aws-snowball-service-and-when-is-it-used)
 39. [Describe AWS CodePipeline and its components.](#describe-aws-codepipeline-and-its-components)
 40. [What is AWS DataSync, and how does it work?](#what-is-aws-datasync-and-how-does-it-work)
 41. [Explain the concept of AWS Auto Scaling.](#explain-the-concept-of-aws-auto-scaling)
 42. [How do you set up AWS Cross-Region Replication for S3?](#how-do-you-set-up-aws-cross-region-replication-for-s3)
 43. [What is Amazon Inspector, and how does it enhance security?](#what-is-amazon-inspector-and-how-does-it-enhance-security)
 44. [Describe AWS App Runner and its use cases.](#describe-aws-app-runner-and-its-use-cases)
 45. [How do you back up and restore AWS RDS databases?](#how-do-you-back-up-and-restore-aws-rds-databases)
 46. [What is Amazon S3 Select?](#what-is-amazon-s3-select)
 47. [Explain the features of Amazon EKS (Elastic Kubernetes Service).](#explain-the-features-of-amazon-eks-elastic-kubernetes-service)
 48. [How do you deploy a serverless application using AWS SAM?](#how-do-you-deploy-a-serverless-application-using-aws-sam)
 49. [Describe AWS Key Management Service (KMS) and its role in encryption.](#describe-aws-key-management-service-kms-and-its-role-in-encryption)
 50. [What is the AWS Lambda Dead Letter Queue (DLQ)?](#what-is-the-aws-lambda-dead-letter-queue-dlq)
 51. [How does AWS WAF (Web Application Firewall) work?](#how-does-aws-waf-web-application-firewall-work)
 52. [What is AWS Glue, and how is it used for data transformation?](#what-is-aws-glue-and-how-is-it-used-for-data-transformation)
 53. [Explain AWS Shield and its role in DDoS protection.](#explain-aws-shield-and-its-role-in-ddos-protection)
 54. [Describe AWS CodeCommit, CodeBuild, and CodeDeploy.](#describe-aws-codecommit-codebuild-and-codedeploy)
 55. [How do you implement disaster recovery in AWS?](#how-do-you-implement-disaster-recovery-in-aws)
 56. [What is Amazon Cognito, and how is it used for user authentication?](#what-is-amazon-cognito-and-how-is-it-used-for-user-authentication)
 57. [How do you create a custom Amazon Machine Image (AMI)?](#how-do-you-create-a-custom-amazon-machine-image-ami)
 58. [Explain the concept of AWS Transit Gateway.](#explain-the-concept-of-aws-transit-gateway)
 59. [What is AWS X-Ray, and how does it help in application tracing?](#what-is-aws-x-ray-and-how-does-it-help-in-application-tracing)
 60. [How do you optimize an AWS S3 bucket for cost and performance?](#how-do-you-optimize-an-aws-s3-bucket-for-cost-and-performance)
 61. [Describe AWS Systems Manager and its features.](#describe-aws-systems-manager-and-its-features)
 62. [What is the AWS Snowball Edge device?](#what-is-the-aws-snowball-edge-device)
 63. [How does Amazon CloudFront work for content delivery?](#how-does-amazon-cloudfront-work-for-content-delivery)
 64. [What are AWS Resource Groups, and how do they simplify resource management?](#what-are-aws-resource-groups-and-how-do-they-simplify-resource-management)
 65. [Explain the features of AWS Step Functions.](#explain-the-features-of-aws-step-functions)
 66. [What is the difference between Amazon Kinesis Data Streams and Kinesis Firehose?](#what-is-the-difference-between-amazon-kinesis-data-streams-and-kinesis-firehose)
 67. [How do you implement high availability in AWS?](#how-do-you-implement-high-availability-in-aws)
 68. [Describe the use cases for AWS Greengrass.](#describe-the-use-cases-for-aws-greengrass)
 69. [What is AWS Global Accelerator, and when is it used?](#what-is-aws-global-accelerator-and-when-is-it-used)
 70. [How do you secure data in Amazon S3 buckets?](#how-do-you-secure-data-in-amazon-s3-buckets)
 71. [Explain the concept of AWS Elemental MediaConvert.](#explain-the-concept-of-aws-elemental-mediaconvert)
 72. [What is Amazon DocumentDB, and how does it differ from MongoDB?](#what-is-amazon-documentdb-and-how-does-it-differ-from-mongodb)
 73. [How do you create a VPC peering connection in AWS?](#how-do-you-create-a-vpc-peering-connection-in-aws)
 74. [Describe the features of AWS Lambda@Edge.](#describe-the-features-of-aws-lambdaedge)
 75. [What is AWS Fargate and how is it different from ECS?](#what-is-aws-fargate-and-how-is-it-different-from-ecs)
 76. [How does AWS Artifact enhance compliance and security?](#how-does-aws-artifact-enhance-compliance-and-security)
 77. [What is AWS PrivateLink, and how does it improve network security?](#what-is-aws-privatelink-and-how-does-it-improve-network-security)
 78. [Explain the use of AWS Greengrass Core.](#explain-the-use-of-aws-greengrass-core)
 79. [How do you set up AWS IAM Identity Center (formerly AWS SSO)?](#how-do-you-set-up-aws-iam-identity-center-formerly-aws-sso)
 80. [What is AWS Cost Explorer, and how does it help in cost analysis?](#what-is-aws-cost-explorer-and-how-does-it-help-in-cost-analysis)
 81. [Describe the use cases for AWS Organizations.](#describe-the-use-cases-for-aws-organizations)
 82. [What is the AWS CDK (Cloud Development Kit)?](#what-is-the-aws-cdk-cloud-development-kit)
 83. [How do you implement cross-account access in AWS?](#how-do-you-implement-cross-account-access-in-aws)
 84. [Explain the difference between Amazon Kinesis Data Streams and Kinesis Data Analytics.](#explain-the-difference-between-amazon-kinesis-data-streams-and-kinesis-data-analytics)
 85. [What is AWS Snowmobile, and when is it used?](#what-is-aws-snowmobile-and-when-is-it-used)
 86. [How do you use AWS Elastic Beanstalk with Docker containers?](#how-do-you-use-aws-elastic-beanstalk-with-docker-containers)
 87. [Describe the features of AWS Control Tower.](#describe-the-features-of-aws-control-tower)
 88. [What is the AWS Partner Network (APN), and how does it support customers?](#what-is-the-aws-partner-network-apn-and-how-does-it-support-customers)
 89. [How do you configure Amazon CloudFront with SSL?](#how-do-you-configure-amazon-cloudfront-with-ssl)
 90. [Explain the AWS Elastic Transcoder service.](#explain-the-aws-elastic-transcoder-service)
 91. [What is AWS Transit Gateway Network Manager?](#what-is-aws-transit-gateway-network-manager)
 92. [How does AWS PrivateLink work with service endpoints?](#how-does-aws-privatelink-work-with-service-endpoints)
 93. [Describe AWS DMS (Database Migration Service) and its use cases.](#describe-aws-dms-database-migration-service-and-its-use-cases)
 94. [What is AWS Chime, and how does it facilitate video conferencing?](#what-is-aws-chime-and-how-does-it-facilitate-video-conferencing)
 95. [How do you use AWS Organizations to consolidate billing?](#how-do-you-use-aws-organizations-to-consolidate-billing)
 96. [What is Amazon Polly, and how does it convert text to speech?](#what-is-amazon-polly-and-how-does-it-convert-text-to-speech)
 97. [Explain the concept of AWS EventBridge.](#explain-the-concept-of-aws-eventbridge)
 98. [How do you use AWS Data Pipeline for data integration?](#how-do-you-use-aws-data-pipeline-for-data-integration)
 99. [Describe the features of AWS CodeGuru.](#describe-the-features-of-aws-codeguru)

### What is AWS and how does it work?

AWS is a cloud computing platform that offers a broad set of global compute, storage, database, analytics, application, and deployment services that help organizations move faster, lower IT costs, and scale applications. AWS's services are built to be scalable and reliable, and they can be accessed on demand from anywhere over the internet.

#### How AWS works:

AWS operates a global network of data centers, called regions. Each region consists of one or more Availability Zones (AZs), which are isolated from each other to protect against service disruptions. AWS customers can choose to run their applications in a single region or in multiple regions for higher availability and redundancy.

To use AWS, customers create an AWS account and then sign up for the services they need. AWS offers a pay-as-you-go pricing model, so customers only pay for the resources they use.

### Explain the difference between EC2 and Lambda.

**EC2** (Elastic Compute Cloud) is a compute service that allows customers to launch virtual machines (VMs) in the cloud. EC2 instances can be used to run any type of application, including web servers, databases, and application servers.

**Lambda** is a serverless compute service that allows customers to run code without provisioning or managing servers. Lambda functions are triggered by events, such as HTTP requests, database changes, or S3 object uploads.

#### Key differences between EC2 and Lambda:

| Feature | EC2 | Lambda |
|---|---|---|
| Provisioning | Customers must provision and manage EC2 instances. | Customers do not need to provision or manage servers. |
| Pricing | Customers are billed for EC2 instances based on the instance type, region, and usage. | Customers are billed for Lambda functions based on the number of executions and the amount of memory used. |
| Use cases | EC2 is a good choice for applications that require persistent storage, high performance, or fine-grained control over the server environment. | Lambda is a good choice for event-driven applications, such as serverless web applications, mobile backends, and data processing pipelines. |

### What is the AWS Well-Architected Framework?

The AWS Well-Architected Framework is a set of best practices and design principles that help customers build secure, reliable, efficient, and cost-effective applications on AWS. The framework is divided into six pillars: operational excellence, security, reliability, performance efficiency, cost optimization, and sustainability.

### Describe AWS IAM (Identity and Access Management).

AWS IAM is a service that allows customers to manage access to AWS resources. IAM allows customers to create users and groups, and to assign them permissions to AWS services and resources. IAM also allows customers to control access to AWS resources using policies.

### What is the difference between Amazon RDS and Amazon DynamoDB?

**Amazon RDS** (Relational Database Service) is a managed database service that makes it easy to set up, operate, and scale a relational database in the cloud. Amazon RDS supports a variety of database engines, including MySQL, PostgreSQL, Oracle, and SQL Server.

**Amazon DynamoDB** is a fully managed, serverless, key-value and document NoSQL database with built-in security, backup and restore, and in-memory caching for internet-scale applications. Amazon DynamoDB offers single-digit millisecond performance at any scale.

#### Key differences between Amazon RDS and Amazon DynamoDB:

| Feature | Amazon RDS | Amazon DynamoDB |
|---|---|---|
| Database model | Relational | NoSQL |
| Schema | Required | Optional |
| Consistency | Strong on the primary instance; read replicas are asynchronous | Eventual by default; strongly consistent reads are optional |
| Querying | SQL | Key-value, document, and secondary indexes |
| Use cases | Web applications, enterprise applications, and OLTP workloads | Mobile applications, gaming applications, and IoT applications |

### What are Amazon VPC and subnet?

Amazon VPC (Virtual Private Cloud) is a service that allows customers to create a logically isolated section of the AWS Cloud where they can launch AWS resources in a private network. A VPC can be used to create a secure and isolated environment for running applications, storing data, and deploying development environments.

A subnet is a range of IP addresses within a VPC. Each subnet is located in exactly one Availability Zone. Subnets are used to group AWS resources together and to control how they interact with each other. For example, you could create a subnet for your web servers and another subnet for your database servers.

### What is the significance of an AWS Availability Zone?

An AWS Availability Zone (AZ) is a physically isolated location within a region. Each AZ has its own power supply, cooling, and networking infrastructure. AZs are designed to be highly reliable and to isolate applications from failures in other AZs.

When you launch an AWS resource, such as an EC2 instance, you can choose to launch it in a specific AZ. This helps you to ensure that your applications are highly available and to protect them from failures in other AZs.

### What is an S3 bucket?

An Amazon S3 bucket is a container for objects (files and their metadata) in a specific AWS Region. Bucket names are globally unique. Buckets commonly hold web assets, images, videos, and backups.

Buckets support versioning, default encryption, and lifecycle rules.

### What is Amazon CloudWatch, and how is it used?

Amazon CloudWatch is a monitoring and observability service that provides data and insights to help customers monitor their AWS resources and applications. CloudWatch collects metrics, logs, and events from AWS resources and applications, and then stores this data in a secure and highly available data store.

CloudWatch can be used to monitor a variety of things, such as CPU utilization, network traffic, disk I/O, and application errors. Memory and disk-space metrics are not published for EC2 instances by default and require the CloudWatch agent. CloudWatch also provides alarms, dashboards, and Logs Insights queries for analyzing log data.

### Define the term "Elastic Load Balancing" in AWS.

Elastic Load Balancing (ELB) distributes incoming traffic across registered targets, such as EC2 instances, IP addresses, Lambda functions, and containers. It sends requests only to healthy targets, which improves availability.

A load balancer distributes traffic across the Availability Zones it is enabled in, within one Region. For routing across Regions, use Route 53 or AWS Global Accelerator. ELB provides health checks and sticky sessions (on ALB and CLB). Automatic scaling is done by EC2 Auto Scaling, not by ELB.

### What is AWS Elastic Beanstalk, and how does it work?

AWS Elastic Beanstalk is a platform that makes it easy to deploy and manage web applications on AWS. Elastic Beanstalk takes care of all the infrastructure details, such as provisioning and managing servers, load balancing, and auto scaling. This allows developers to focus on writing and deploying their applications.

To use Elastic Beanstalk, developers create an application and then choose a platform (such as Java, PHP, or Ruby). Elastic Beanstalk will then create the necessary infrastructure and deploy the application.

### Describe the use cases for Amazon SNS and Amazon SQS.

Amazon SNS (Simple Notification Service) is a pub/sub messaging service. Publishers send messages to a topic, and SNS delivers them to subscribers such as SQS queues, Lambda functions, HTTP/S endpoints, email, and SMS.

Amazon SQS (Simple Queue Service) is a fully managed message queue. Producers send messages to a queue, and consumers poll and process them asynchronously. Standard queues offer at-least-once delivery with best-effort ordering. FIFO queues provide exactly-once processing and ordering within a message group.

#### Use cases for Amazon SNS:

* Sending notifications to users, such as email, SMS, or push notifications.
* Decoupling microservices by sending messages between them.
* Triggering AWS Lambda functions.

#### Use cases for Amazon SQS:

* Decoupling microservices by asynchronously exchanging messages between them.
* Buffering messages between applications.
* Holding messages that fail processing in a dead-letter queue (DLQ) after a set number of receives.

### How does AWS Lambda handle concurrent executions?

Lambda runs each in-flight request in its own execution environment, so concurrency is the number of requests being processed at once. The default account quota is 1,000 concurrent executions per Region, and it can be raised. New accounts can start with lower quotas.

Reserved concurrency caps a function's concurrency and reserves capacity for it. Provisioned concurrency keeps initialized environments ready to avoid cold starts. Requests above the limit are throttled for synchronous invocations and retried for asynchronous ones.

### What are AWS CloudFormation templates, and how do they work?

AWS CloudFormation templates are JSON or YAML files that describe the AWS resources that you want to create. CloudFormation templates can be used to create a wide range of AWS resources, including EC2 instances, RDS databases, and S3 buckets.

To use a CloudFormation template, you first create the template and then deploy it to AWS. CloudFormation will then create the resources that are described in the template.

CloudFormation templates are a good way to automate the deployment of AWS resources. They can also be used to create and manage complex AWS architectures.

### Explain the differences between Amazon S3, EBS, and EFS.

**Amazon S3 (Simple Storage Service)** is object storage. You store objects (files and their metadata) in buckets and access them over HTTP(S) through the S3 API.

**Amazon EBS (Elastic Block Store)** is block storage for EC2 instances. A volume exists in a single Availability Zone and attaches to an instance in that AZ. It can outlive the instance, depending on its DeleteOnTermination setting. Typical uses are boot volumes and databases.

**Amazon EFS (Elastic File System)** is a managed NFS file system. Many EC2 instances, including instances in different AZs, can mount the same file system at once.

#### Differences between Amazon S3, EBS, and EFS:

| Feature | Amazon S3 | Amazon EBS | Amazon EFS |
|---|---|---|---|
| Storage type | Object storage | Block storage | Network file system (NFS) |
| Access | HTTP(S) API | One EC2 instance at a time (Multi-Attach is limited to some io1 and io2 volumes) | Many EC2 instances, mounted over NFS |
| Availability scope | Regional, data stored redundantly across AZs | Single AZ | Regional (One Zone option available) |
| Use cases | Static and dynamic web content, archives, backups, disaster recovery | Boot volumes, databases, application files | Files shared across multiple EC2 instances |

### How do you secure your AWS resources using Security Groups and NACLs?

Security groups and NACLs are two complementary security features that can be used to protect your AWS resources.

**Security groups** are stateful firewalls attached to resources such as EC2 instances, RDS databases, and load balancers. They contain allow rules only, and return traffic is allowed automatically. You can change the groups attached to a resource at any time.

**NACLs (Network Access Control Lists)** are stateless firewalls attached to subnets. They have numbered allow and deny rules evaluated in order, and return traffic must be allowed explicitly.

To secure your AWS resources using security groups and NACLs, you can follow these best practices:

* **Use security groups to control inbound and outbound traffic to your EC2 instances.** Only allow the traffic that is necessary for your applications to function.
* **Use NACLs to control inbound and outbound traffic at the subnet level.** This can help to protect your resources from unauthorized access.
* **Use least privilege.** Only grant users the permissions that they need to perform their jobs.
* **Monitor your security groups and NACLs regularly.** Make sure that they are still meeting your security needs.

### What is Amazon Aurora, and how does it differ from other databases?

Amazon Aurora is a fully managed relational database that combines the performance and availability of high-end commercial databases with the simplicity and cost-effectiveness of open source databases. AWS states that Aurora can be up to five times faster than standard MySQL and up to three times faster than standard PostgreSQL. Multi-AZ clusters carry a 99.99% monthly uptime SLA.

Aurora separates compute from a distributed storage layer that keeps six copies of the data across three AZs. This storage design is the main difference from standard RDS engines.

### Describe the AWS Global Accelerator service.

AWS Global Accelerator gives your application static anycast IP addresses. Client traffic enters the AWS global network at the edge location nearest the user and travels over the AWS backbone to the nearest healthy regional endpoint, such as an ALB, NLB, EC2 instance, or Elastic IP address.

It suits applications that need static IP addresses, fast regional failover, or TCP and UDP traffic, such as gaming and real-time services.

### What is the AWS Trusted Advisor?

AWS Trusted Advisor is a service that helps you to improve the security, performance, and cost-effectiveness of your AWS resources. Trusted Advisor analyzes your AWS resources and provides recommendations for improvement.

Checks cover cost optimization, performance, security, fault tolerance, and service limits. Basic and Developer support plans get only the core checks. Business and Enterprise plans get the full set.

### How does AWS handle data encryption at rest and in transit?

AWS offers a variety of data encryption features to help you to protect your data at rest and in transit.

**Data encryption at rest** means that your data is encrypted when it is stored on AWS servers. AWS uses a variety of encryption algorithms, including AES-256, to encrypt your data at rest.

**Data encryption in transit** means that your data is encrypted when it is transmitted over the network. AWS uses a variety of protocols, such as HTTPS and TLS, to encrypt your data in transit.

You can also use customer managed keys (CMKs) in AWS KMS to encrypt data at rest. CMKs let you control key policies, aliases, and rotation, subject to IAM permissions and KMS safeguards. Encryption in transit comes from TLS, not from KMS keys.

### Explain the significance of Amazon Route 53.

Amazon Route 53 is a highly available and scalable DNS service that can be used to route traffic to your applications and websites. Route 53 supports a variety of DNS features, such as traffic management, health checks, and failover.

### What is Amazon ElastiCache, and how does it improve application performance?

Amazon ElastiCache is a managed in-memory data store service that improves the performance of web applications by caching frequently accessed data in memory. ElastiCache supports popular in-memory data stores: Memcached, Redis OSS, and Valkey.

Serving repeated reads from the cache reduces database load and read latency. The common pattern is cache-aside: the application checks the cache first and loads from the database on a miss.

### How do you scale an application on AWS?

There are a number of ways to scale an application on AWS. Some common scaling methods include:

* **Horizontal scaling:** This involves adding more instances of your application to handle increased traffic.
* **Vertical scaling:** This involves adding more resources to your existing instances, such as CPU, memory, and storage.
* **Auto Scaling:** An Auto Scaling group adds or removes EC2 instances based on scaling policies or schedules.

### What is the AWS Serverless Application Model (SAM)?

The AWS Serverless Application Model (SAM) is a framework for building and deploying serverless applications on AWS. SAM provides a high-level abstraction for serverless applications, which can make it easier to develop and deploy serverless applications.

SAM templates can be used to define your serverless application and its resources. SAM can then be used to deploy your application to AWS.

### Explain AWS Elastic Container Service (ECS) and Kubernetes.

AWS Elastic Container Service (ECS) is a managed container orchestration service that makes it easy to run Docker containers on AWS. ECS provides a number of features that make it easy to manage your containers, such as task scheduling, load balancing, and health checks.

Kubernetes is an open-source container orchestration platform that automates many of the manual processes involved in managing containers. Kubernetes provides a number of features that make it easy to deploy, manage, and scale containerized applications.

Amazon EKS is AWS's managed Kubernetes service. ECS uses AWS-native task definitions and services. Choose ECS for an AWS-only workflow, and EKS when you need Kubernetes APIs or tooling.

### Describe the features of Amazon Redshift.

Amazon Redshift is a managed, petabyte-scale data warehouse. It stores data in columns and runs queries in parallel across nodes. You query it with standard SQL and existing BI tools.

Redshift is available as provisioned clusters (RA3 node types) and as Redshift Serverless.

### How does AWS Step Functions work, and what are its use cases?

AWS Step Functions is a serverless workflow orchestration service that makes it easy to build and run state machines and workflows. Step Functions helps you to coordinate the execution of multiple steps across multiple AWS services.

Step Functions works by defining a state machine in Amazon States Language (ASL), a JSON-based language. The state machine defines the steps, their order, and the transitions between them. Workflow Studio provides a visual editor.

Step Functions runs the state machine and passes data between steps. Retry and Catch rules in each state handle errors and retries.

Step Functions can be used to build a variety of workflows, such as:

* Order fulfillment workflows
* Customer onboarding workflows
* Data processing workflows
* Machine learning workflows
* Security incident response workflows

### What is AWS Lambda Layers?

AWS Lambda layers package libraries and other dependencies separately from function code, so they can be shared across functions.

A function can use up to five layers. The unzipped size of the function code plus all of its layers must stay within the 250 MB unzipped deployment package quota.

### How do you migrate an on-premises database to AWS?

There are a number of ways to migrate an on-premises database to AWS. Some common migration methods include:

* **Dump and restore:** Export with a native tool (for example, `pg_dump` or `mysqldump`) and import into RDS or Aurora. This suits small databases that can tolerate downtime.
* **AWS Database Migration Service (DMS):** Full load plus ongoing change data capture (CDC), which keeps the target in sync until cutover.
* **AWS Schema Conversion Tool (SCT):** Converts schema and code for heterogeneous migrations, such as Oracle to PostgreSQL. Use it alongside DMS.

### Explain the use of AWS Direct Connect.

AWS Direct Connect is a private network connection between your on-premises data center and AWS, using a dedicated or hosted connection. Direct Connect does not encrypt traffic by default. For encryption, use MACsec on dedicated connections, or an IPsec Site-to-Site VPN over a public or transit virtual interface, which also works on hosted connections.

Direct Connect can be used for a variety of purposes, such as:

* Migrating data to AWS
* Running hybrid applications
* Accessing AWS services with low latency

### What is AWS Elastic File System (EFS)?

EFS grows and shrinks automatically as files are added and removed. Mount targets in each AZ let instances in different AZs mount the same file system over NFS.

Storage classes include Standard, Infrequent Access (IA), and Archive, with lifecycle management to move files between them. One Zone variants store data in a single AZ.

### Describe the benefits of using AWS CloudTrail.

AWS CloudTrail is a service that records AWS API calls and related events. CloudTrail can be used to audit your AWS account activity and to track changes to your AWS resources.

Event history keeps 90 days of management events per Region with no setup. For longer retention, create a trail that delivers log files to an S3 bucket.

Some of the benefits of using AWS CloudTrail include:

* **Compliance:** CloudTrail can help you to comply with a variety of compliance requirements, such as PCI DSS and HIPAA.
* **Security:** CloudTrail can help you to identify and investigate security threats.
* **Troubleshooting:** CloudTrail can help you to troubleshoot problems with your AWS applications and resources.

### What are the types of Elastic Load Balancing?

Elastic Load Balancing has four load balancer types:

* **Application Load Balancer (ALB):** Layer 7. Routes HTTP and HTTPS requests by path, host, or header.
* **Network Load Balancer (NLB):** Layer 4. Routes TCP, UDP, and TLS traffic and provides a static IP address per Availability Zone.
* **Gateway Load Balancer (GWLB):** Layer 3. Inserts third-party appliances, such as firewalls, into the traffic path.
* **Classic Load Balancer (CLB):** Legacy. Use ALB or NLB for new workloads.

### How do you optimize costs in AWS?

There are a number of ways to optimize costs in AWS. Some common cost optimization techniques include:

* **Choose the right instance type:** AWS offers a variety of instance types, each with a different price-performance ratio. Choose the instance type that is best suited for your workload.
* **Commit to usage:** Savings Plans and Reserved Instances (1- or 3-year terms) give lower prices in exchange for a commitment to steady usage.
* **Spot instances:** Spare EC2 capacity at a discount. AWS can interrupt a Spot instance with a two-minute notice, so use Spot for fault-tolerant work such as batch processing.
* **Use managed services:** AWS offers a variety of managed services that can help you to optimize your costs. For example, Amazon RDS is a managed database service that can help you to reduce the cost of managing your own database servers.
* **Monitor your costs:** Use AWS Cost Explorer to track your AWS costs. Cost Explorer can help you to identify areas where you can optimize your costs.

### What are AWS Organizations, and how are they used?

AWS Organizations is a service that helps you to centrally manage your AWS accounts. Organizations allows you to create accounts for different departments or projects, and to manage permissions for those accounts.

Service control policies (SCPs) set the maximum permissions for accounts in an organization, and consolidated billing combines charges for all member accounts.

### Explain the benefits of using AWS Fargate.

AWS Fargate is a serverless compute engine for Docker containers. Fargate makes it easy to run Docker containers on AWS without having to manage servers.

Some of the benefits of using AWS Fargate include:

* **Reduced operational overhead:** Fargate manages the servers and infrastructure that are needed to run your containers, so you don't have to worry about managing them yourself.
* **Improved scalability:** Fargate provisions the compute for your tasks automatically, and ECS Service Auto Scaling can adjust the number of tasks to meet demand.
* **Increased security:** Fargate isolates your containers from each other and from the underlying infrastructure, which helps to improve security.

### How do you monitor AWS resources using CloudWatch Alarms?

CloudWatch Alarms is a service that allows you to monitor your AWS resources and send notifications when certain conditions are met. For example, you could create a CloudWatch Alarm to notify you when your CPU utilization exceeds a certain threshold.

Alarms can watch any metric, such as CPU utilization, network traffic, or RDS database connections. An alarm moves between OK, ALARM, and INSUFFICIENT_DATA states and can notify an SNS topic. Memory is a custom metric that comes from the CloudWatch agent.

### AWS Snowball service and when is it used?

AWS Snowball was a service for moving large datasets to AWS offline, using shipped devices. AWS no longer accepts new Snow Family orders, and support for Snowball Edge is ending. For new bulk transfers, use AWS DataSync over the network. Check the Snowball Edge availability change notice in the AWS docs before planning any Snowball job.

### Describe AWS CodePipeline and its components.

AWS CodePipeline is a continuous delivery service that helps you to automate the release and deployment process for your applications. CodePipeline orchestrates the workflow: it invokes other services, such as CodeBuild for building and testing and CodeDeploy for deployments, every time there is a change.

CodePipeline consists of the following components:

* **Pipeline:** A pipeline is a sequence of stages that define the build, test, and deploy process for your application.
* **Stage:** A logical group of actions, such as Source, Build, Test, or Deploy. A stage runs its actions before the pipeline moves on to the next stage.
* **Action:** A task inside a stage, such as a CodeBuild build or a CodeDeploy deployment. Action categories are Source, Build, Test, Deploy, Approval, and Invoke.

### What is AWS DataSync, and how does it work?

AWS DataSync is a service that helps you to automate the transfer of data between on-premises storage systems and AWS storage services. DataSync copies to and from on-premises NFS and SMB file shares, HDFS, and self-managed object storage through a DataSync agent. DataSync also supports a variety of AWS storage services, including S3, EFS, and FSx.

DataSync works by creating a task that defines the source location, the destination location, and the configuration and schedule for the transfer. Each task execution copies the data you specify; recurring executions can be scheduled, but DataSync does not continuously monitor the source for changes.

### Explain the concept of AWS Auto Scaling.

AWS Auto Scaling is a service that automatically scales your applications based on demand. Auto Scaling adds or removes capacity as demand changes.

Auto Scaling works by monitoring your applications and scaling them based on predefined metrics. For example, you could configure Auto Scaling to scale your application up when CPU utilization exceeds a certain threshold.

### How do you set up AWS Cross-Region Replication for S3?

S3 Cross-Region Replication (CRR) is a bucket-level feature that asynchronously copies new objects to a bucket in another Region. It helps protect data against a regional outage.

Setup:

1. Enable versioning on the source and destination buckets.
2. Create an IAM role that S3 can assume to replicate objects.
3. Add a replication rule to the source bucket that names the destination bucket.

Optionally, enable Replication Time Control (RTC) to replicate 99.9% of objects within 15 minutes.

### What is Amazon Inspector, and how does it enhance security?

Amazon Inspector is a service that helps you to identify and remediate security vulnerabilities in your AWS resources. Inspector scans your resources for vulnerabilities and provides you with a report of the findings.

Inspector covers EC2 instances, container images in Amazon ECR, and Lambda functions. Findings are rated by severity and include remediation guidance.

### Describe AWS App Runner and its use cases.

AWS App Runner is a fully managed service that makes it easy to deploy, run, and scale web applications and APIs. App Runner manages the build, deployment, and scaling of your service. It deploys from a source repository or a container image.

App Runner suits web applications and APIs that do not need custom infrastructure.

### How do you back up and restore AWS RDS databases?

There are two ways to back up and restore AWS RDS databases:

* **Automated backups:** RDS takes a daily snapshot during the backup window and uploads transaction logs about every five minutes. Together they enable point-in-time recovery (PITR). You set the retention period from 0 to 35 days; 0 disables automated backups.
* **Manual snapshots:** Created on demand and kept until you delete them.

Restoring (PITR or from a snapshot) creates a new DB instance with a new endpoint. You choose the instance class for it, and the application must point to the new endpoint.

### What is Amazon S3 Select?

Amazon S3 Select is a feature that lets you retrieve a subset of data from an S3 object using simple SQL expressions, without downloading the entire object. This can save time and bandwidth, especially when you are processing large objects.

Note that AWS closed S3 Select to new customers on July 25, 2024, and it supports a limited subset of SQL (filtering and projecting columns) on one object at a time rather than general-purpose data processing. Existing customers can keep using it, but AWS does not add new features. For new work, consider Amazon Athena or S3 Object Lambda.

### Explain the features of Amazon EKS (Elastic Kubernetes Service).

Amazon EKS is a managed Kubernetes service that makes it easy to deploy, run, and scale Kubernetes applications on AWS. EKS manages the Kubernetes control plane for you. You still manage worker nodes unless you use managed node groups or AWS Fargate.

EKS provides a number of features that make it a good choice for running Kubernetes applications, including:

* **Scalability:** EKS can scale your Kubernetes clusters to meet demand.
* **Security:** EKS provides a number of security features to protect your Kubernetes applications, such as encryption and role-based access control (RBAC).
* **Integrations:** EKS integrates with a variety of AWS services, such as Amazon S3, Amazon EBS, and Amazon CloudWatch.

### How do you deploy a serverless application using AWS SAM?

SAM is an extension of CloudFormation for serverless resources, such as functions and APIs. You deploy it with the SAM CLI.

To deploy a serverless application using SAM, you first need to create a SAM template. A SAM template is a JSON or YAML file that defines your serverless application and its resources.

Run `sam build` to build the functions and layers into `.aws-sam`, then run `sam deploy --guided` for the first deployment. The guided prompts ask for a stack name, Region, and whether SAM can create IAM roles. They save the answers to `samconfig.toml`, so later runs can use `sam deploy`.

### Describe AWS Key Management Service (KMS) and its role in encryption.

AWS Key Management Service (KMS) is a managed service that makes it easy to create and control the cryptographic keys that are used to protect your data. KMS protects its keys in hardware security modules (HSMs) that are validated to FIPS 140-3 Security Level 3.

KMS plays a crucial role in encryption by providing a centralized and secure way to manage encryption keys. Services such as S3, EBS, and RDS encrypt data at rest with KMS keys once you enable encryption for them. Access to keys is controlled through key policies and IAM.

KMS can be used to encrypt a variety of data types, including:

* EBS volumes
* S3 objects
* RDS databases
* ElastiCache clusters
* Kinesis streams
* DynamoDB tables

### What is the AWS Lambda Dead Letter Queue (DLQ)?

The AWS Lambda Dead Letter Queue (DLQ) is an Amazon SQS queue or Amazon SNS topic that receives events from asynchronous invocations that Lambda cannot process successfully. This can happen when:

* The function returns an error on every attempt, including timeouts.
* The event stays in the asynchronous invocation queue longer than the maximum event age.

When a function is invoked asynchronously, Lambda retries failed events (two retries by default), and the DLQ receives the events after those retries are exhausted so you can inspect and reprocess them. AWS recommends on-failure destinations for new functions, which can be used instead of or alongside a DLQ.

### How does AWS WAF (Web Application Firewall) work?

AWS WAF is a web application firewall that helps to protect your web applications from common attack vectors, such as SQL injection and cross-site scripting (XSS). Rate-based rules can also limit HTTP floods.

WAF works by inspecting incoming HTTP and HTTPS traffic and filtering out malicious requests. You associate a web ACL with supported resources, such as CloudFront distributions, API Gateway REST APIs, Application Load Balancers, AWS AppSync, or App Runner services.

### What is AWS Glue, and how is it used for data transformation?

AWS Glue is a fully managed data integration service that makes it easy to discover, prepare, load, and analyze data. Glue provides a variety of tools and features for data transformation, including:

* **Data catalog:** Glue provides a data catalog that helps you to discover and manage your data.
* **Data crawlers:** Glue provides data crawlers that can scan your data sources and create a schema for your data.
* **ETL jobs:** Glue jobs run Spark or Python shell scripts that clean, transform, and load your data into a target data store.
* **Workflows:** Glue workflows chain crawlers and jobs together so they run as one pipeline.

### Explain AWS Shield and its role in DDoS protection.

AWS Shield is a managed DDoS protection service that protects your web applications from DDoS attacks. Shield provides two layers of protection:

* **Shield Standard:** Shield Standard is included with all AWS accounts and provides basic protection against DDoS attacks.
* **Shield Advanced:** Shield Advanced is a paid service that provides advanced protection against DDoS attacks.

Shield Standard applies automatic protection against common network and transport layer attacks at no additional cost. Shield Advanced adds attack visibility, access to the AWS DDoS Response Team, and cost protection for scaling charges. It requires a one-year commitment and a monthly fee, plus data transfer charges. Scaling your infrastructure to absorb legitimate traffic during an attack is handled separately, for example with Auto Scaling.

### Describe AWS CodeCommit, CodeBuild, and CodeDeploy.

AWS CodeCommit is a managed Git repository service. AWS closed CodeCommit to new customers on July 25, 2024, and the CodeCommit user guide lists it as available to new customers again from November 25, 2025. CodeCommit provides the following features:

* **Security:** CodeCommit encrypts your code at rest and in transit.
* **Integrations:** CodeCommit integrates with a variety of AWS services, such as CodeBuild and CodeDeploy.

AWS CodeBuild is a managed build service that makes it easy to build and test your code. CodeBuild can build and test your code on a variety of platforms, including Linux, Windows, and macOS.

CodeBuild can also be integrated with other AWS services, such as CodeCommit and CodeDeploy, to automate your build and test pipeline.

AWS CodeDeploy is a managed deployment service that makes it easy to deploy your code to a variety of AWS services, such as EC2, Lambda, and ECS. CodeDeploy provides a number of features that make it easy to deploy your code, such as:

* **Blue/green deployments:** CodeDeploy can perform blue/green deployments, which allows you to safely deploy your code without disrupting your production environment.
* **Rollbacks:** CodeDeploy can roll back your deployments in case of a problem.
* **Integrations:** CodeDeploy integrates with a variety of AWS services, such as CodeCommit and CodeBuild.

Together with AWS CodePipeline, which orchestrates the stages, CodeCommit, CodeBuild, and CodeDeploy form a continuous integration and continuous delivery (CI/CD) pipeline.

### How do you implement disaster recovery in AWS?

To implement disaster recovery in AWS, you can follow these steps:

1. **Define your recovery time objective (RTO) and recovery point objective (RPO).** The RTO is the maximum amount of time that your applications can be unavailable after a disaster. The RPO is the maximum acceptable amount of time since the last data recovery point, in other words how much data you can afford to lose.
2. **Choose a disaster recovery strategy.** The commonly used strategies are backup and restore, pilot light, warm standby, and multi-site active/active. They differ in how much of your environment is kept running in a second Region, and in their relative cost and recovery time.
3. **Implement your disaster recovery strategy.** There are a number of AWS services that can help you implement your disaster recovery strategy, such as:

* AWS Elastic Disaster Recovery (AWS DRS): continuously replicates source servers to AWS so you can recover them quickly into a secondary Region.
* AWS Backup: a fully managed backup service that centralizes backup policies and protects data across AWS services.
* Amazon Route 53: health checks and failover routing that shift traffic to the recovery Region.
* AWS CloudFormation: AWS CloudFormation is a managed service that helps you model and provision AWS resources in a consistent and repeatable way.

4. **Test your disaster recovery plan.** It is important to test your disaster recovery plan regularly to ensure that it works as expected.

Here is an example of how to implement a pilot light disaster recovery strategy in AWS:

1. Create a VPC in a separate AWS Region.
2. Launch a few EC2 instances in the VPC.
3. Install and configure your application on the EC2 instances.
4. Configure data replication between your production environment and the disaster recovery environment.
5. Test the data replication process to ensure that it is working as expected.
6. Regularly test the disaster recovery plan by failing over to the disaster recovery environment.

When a disaster occurs, fail over by updating DNS (for example, with Route 53 failover routing) so that traffic reaches the recovery environment.

After the primary Region is restored, fail back by synchronizing data to the primary environment and updating DNS again.

### What is Amazon Cognito, and how is it used for user authentication?

Amazon Cognito is a managed user identity and access management service that makes it easy to add user authentication and authorization to your web and mobile applications. Cognito provides a number of features that make it easy to authenticate users, including:

* **Social login:** Cognito allows users to log in to your applications using their social media accounts, such as Apple, Facebook, Google, and Amazon, as well as SAML and OIDC identity providers.
* **Hosted sign-in:** Cognito provides a hosted sign-in UI that you can customize, or you can build your own UI on the Cognito APIs.
* **Multi-factor authentication (MFA):** Cognito supports MFA to help protect your users' accounts from unauthorized access.

Identity pools exchange user tokens for temporary AWS credentials. IAM roles attached to those credentials control access to services such as S3 and DynamoDB.

### How do you create a custom Amazon Machine Image (AMI)?

An Amazon Machine Image (AMI) is a template that contains a preconfigured operating system and applications. AMIs can be used to launch EC2 instances.

To create a custom AMI, you can use the EC2 Image Builder service. EC2 Image Builder allows you to create AMIs from a base image using a recipe.

EC2 Image Builder also provides a number of features that make it easy to create custom AMIs, such as:

* **Recipes:** Recipes define the base image and the components applied to it.
* **Components:** Components are versioned documents (YAML or JSON) that define the build and test steps, such as installing software.
* **Infrastructure and distribution settings:** Infrastructure configuration sets the instance type and subnet used for the build. Distribution configuration sets the AMI name, description, and target Regions and accounts.

Once you have created a custom AMI, you can launch EC2 instances from it.

### Explain the concept of AWS Transit Gateway.

AWS Transit Gateway is a network transit hub that makes it easy to connect your VPCs, on-premises networks, and other AWS services. Transit Gateway provides a central place to manage your network routing and to connect your network resources.

Transit Gateway routes traffic between attachments such as VPCs, VPN connections, and Direct Connect gateways, and its route tables control which attachments can reach each other.

Here are some of the benefits of using AWS Transit Gateway:

* **Centralized network routing:** Transit Gateway provides a central place to manage your network routing. This makes it easier to configure and manage your network.
* **Attachments:** VPCs, VPN connections, Direct Connect gateways, and peering with other Transit Gateways, including in other Regions.
* **Segmentation:** Separate route tables isolate groups of attachments from each other.

### What is AWS X-Ray, and how does it help in application tracing?

AWS X-Ray is a service that helps you to debug and monitor your distributed applications. X-Ray provides a detailed view of your application's traces, which are records of how requests flow through your application.

X-Ray can be used to identify performance bottlenecks, troubleshoot errors, and understand the behavior of your application. The X-Ray SDKs and daemon entered maintenance mode on February 25, 2026. AWS recommends OpenTelemetry instrumentation for new work.

Here are some of the benefits of using AWS X-Ray:

* **Identify performance bottlenecks:** X-Ray can help you to identify performance bottlenecks in your application.
* **Troubleshoot errors:** X-Ray can help you to troubleshoot errors in your application.
* **Understand application behavior:** X-Ray can help you to understand the behavior of your application by providing a detailed view of your application's traces.

### How do you optimize an AWS S3 bucket for cost and performance?

There are a number of things you can do to optimize your AWS S3 buckets for cost and performance.

Here are some tips:

* **Use the right storage class:** S3 offers a variety of storage classes, each with its own pricing and performance characteristics. Choose the storage class that is right for your needs.
* **Use lifecycle rules:** S3 Lifecycle rules transition objects to lower-cost storage classes or expire them automatically, based on age or usage patterns.
* **Use versioning:** S3 versioning keeps earlier versions of objects, which protects against accidental overwrites and deletes. Noncurrent versions add storage cost, so pair versioning with lifecycle rules that expire them.
* **Use compression:** Compressing your objects before storing them in S3 can reduce your storage costs.
* **Use CloudFront for delivery:** Serving frequently read objects through Amazon CloudFront caches them near users, which lowers latency and reduces load on the bucket.

### Describe AWS Systems Manager and its features.

AWS Systems Manager is a service that helps you to manage your AWS resources. Systems Manager provides a number of features that make it easier to manage your resources, such as:

* **Inventory:** Inventory collects software and configuration metadata from managed nodes.
* **Patching:** Patch Manager applies patches to managed nodes on a schedule.
* **Configuration:** State Manager keeps managed nodes in a defined state.
* **Automation:** Automation runbooks run multi-step tasks across resources.
* **Session Manager:** Session Manager provides shell access to instances without opening SSH ports or using a bastion host.

### What is the AWS Snowball Edge device?

AWS Snowball Edge is a device that can be used to transfer data to and from AWS. AWS stopped accepting new Snowball Edge customers on November 7, 2025. Existing customers can keep using the service. For new transfers, use AWS DataSync for online transfers, AWS Data Transfer Terminal for physical transfers, or AWS Partner solutions for offline transfers.

Existing Snowball Edge devices can still run edge computing applications; AWS recommends AWS Outposts for new edge deployments. Edge computing applications are applications that are run on devices that are located close to the data source. This can reduce latency and improve performance.

### How does Amazon CloudFront work for content delivery?

Amazon CloudFront is a content delivery network (CDN) that can be used to deliver content to users around the world with low latency and high performance. CloudFront works by caching content at edge locations around the world. When a user requests content, CloudFront delivers the content from the edge location that is closest to the user.

CloudFront can be used to deliver a variety of content, such as web pages, images, videos, and static files. CloudFront can also be used to deliver dynamic content, such as streaming video and live events.

### What are AWS Resource Groups, and how do they simplify resource management?

AWS Resource Groups are a way to group your AWS resources together so you can manage them as a set. Resource groups are not an access-control boundary; to grant permissions by tag, use IAM condition keys such as aws:ResourceTag.

Resource Groups can be used to group resources by application, by environment, or by any other criteria that makes sense for you.

### Explain the features of AWS Step Functions.

AWS Step Functions is a service that makes it easy to build and run state machines and workflows. Step Functions can be used to orchestrate the execution of multiple steps across multiple AWS services.

Step Functions provides a number of features that make it easy to build and run state machines and workflows, including:

* **Visual workflow designer:** Step Functions provides a visual workflow designer that makes it easy to create and edit state machines.
* **Error handling and retries:** Step Functions lets you define Retry and Catch behavior per state, so failed steps can be retried or handled according to your workflow.
* **Standard and Express workflows:** Standard workflows run for up to one year and suit long-running, auditable processes. Express workflows run for up to five minutes and suit high-volume, short-lived work.
* **Integration with other AWS services:** Step Functions integrates with a variety of other AWS services, such as Lambda, ECS, and DynamoDB.

### What is the difference between Amazon Kinesis Data Streams and Kinesis Firehose?

Amazon Kinesis Data Streams and Amazon Data Firehose are both services for ingesting and processing streaming data. However, there are some key differences between the two services.

Kinesis Data Streams is a real-time data streaming service that can be used to ingest and process streaming data from a variety of sources, such as web applications, sensors, and social media feeds. Kinesis Data Streams provides a durable and scalable platform for processing streaming data in real time. Records are retained for 24 hours by default. You can extend retention up to 365 days, which incurs additional charges.

Amazon Data Firehose (formerly Amazon Kinesis Data Firehose) is a near-real-time data ingestion service that can be used to ingest and load data into data lakes, data warehouses, and other analytics destinations. It automatically buffers and delivers data; record transformation and format conversion can be enabled when needed.

To choose between Kinesis Data Streams and Amazon Data Firehose, you need to consider your specific needs and requirements. If you need to process data in real time, then Kinesis Data Streams is the better choice. If you need to load streaming data into data stores or analytics services, then Amazon Data Firehose is the better choice.

Here are some examples of when to use Kinesis Data Streams:

* To build a real-time stock trading application.
* To build a social media monitoring application that analyzes tweets and other social media posts in real time.
* To build a fraud detection application that analyzes transactions in real time to identify fraudulent activity.

Here are some examples of when to use Amazon Data Firehose:

* To load streaming data into a data lake, such as Amazon S3.
* To load streaming data into a data store, such as Amazon Redshift or Amazon OpenSearch Service.
* To load streaming data into a supported destination, such as Splunk, or Amazon S3 for querying with Athena.

### How do you implement high availability in AWS?

There are a number of ways to implement high availability in AWS. Some common methods include:

* **Redundancy:** Deploy your applications and data across multiple Availability Zones (AZs). This will help to protect your applications and data from AZ outages.
* **Load balancing:** Use load balancers to distribute traffic across your applications. This will help to improve the performance and availability of your applications.
* **Auto Scaling:** Use Auto Scaling to add or remove capacity based on demand, which helps keep capacity matched to load.
* **Disaster recovery:** Develop a disaster recovery plan to help you recover from a disaster, such as a regional outage or a natural disaster.

### Describe the use cases for AWS Greengrass.

AWS IoT Greengrass is a service that extends AWS cloud capabilities to local devices. It allows devices to collect and analyze data closer to the source, while also securely communicating with each other on local networks.

Common use cases for AWS IoT Greengrass include:

* **Industrial IoT:** Greengrass can be used to connect and manage industrial IoT devices, such as sensors and actuators.* **Smart cities:** Greengrass can be used to connect and manage smart city infrastructure, such as traffic lights, public transportation, and waste management systems.* **Retail:** Greengrass can be used to connect and manage retail devices, such as smart carts, cameras, and mobile apps.* **Healthcare:** Greengrass can be used to connect and manage healthcare devices, such as wearable devices and medical equipment.
### What is AWS Global Accelerator, and when is it used?

AWS Global Accelerator is a service that improves the performance and availability of your global applications. It routes user traffic over the AWS global network to the nearest healthy endpoint in your endpoint groups, which can reduce latency and improve availability for users around the world.

Global Accelerator suits TCP and UDP workloads, such as gaming, VoIP, and IoT, that need static IP addresses and fast failover across Regions. For HTTP content delivery and caching, CloudFront is usually the better fit.

### How do you secure data in Amazon S3 buckets?

There are a number of ways to secure data in Amazon S3 buckets. Some common methods include:

* **Server-side encryption (SSE):** SSE encrypts data at rest. The options are SSE-S3 (keys managed by S3), SSE-KMS (AWS KMS keys, including customer managed keys), and SSE-C (keys you provide with each request). Since January 2023, Amazon S3 applies SSE-S3 to all new objects by default.
* **Client-side encryption (CSE):** CSE encrypts your data before it is uploaded to S3, using keys from AWS KMS or keys that your application manages.
* **Bucket policies:** Bucket policies can be used to control access to your S3 buckets. You can use bucket policies to restrict who can access your buckets and what they can do with them.
* **Block Public Access:** Block Public Access settings override bucket policies and ACLs that would make data public.
* **Object ACLs:** Object ACLs can be used to control access to individual objects in your S3 buckets. You can use object ACLs to restrict who can access the objects and what they can do with them. AWS recommends disabling ACLs where possible, and new buckets have ACLs disabled by default.

### Explain the concept of AWS Elemental MediaConvert.

AWS Elemental MediaConvert is a service that converts video files from one format to another. MediaConvert can also be used to generate thumbnails, transcode audio, and create captions.

MediaConvert is a good choice for converting video files for different devices and platforms. It is also a good choice for generating thumbnails and transcoding audio.

### What is Amazon DocumentDB, and how does it differ from MongoDB?

Amazon DocumentDB is a fully managed document database service that is compatible with MongoDB. DocumentDB provides a scalable, reliable, and secure way to run MongoDB workloads.

DocumentDB implements the MongoDB API, but it is not the MongoDB engine. It supports a subset of MongoDB features and operators, so check the compatibility list for the version you run (4.0, 5.0, and 8.0 are supported). AWS manages the infrastructure, patching, and backups.

DocumentDB is a good choice for running MongoDB workloads that require high scalability, reliability, and security.

### How do you create a VPC peering connection in AWS?

To create a VPC peering connection in AWS, follow these steps:

1. Open the Amazon VPC console.
2. In the navigation pane, choose **Peering connections**.
3. Choose **Create peering connection**.
4. Choose the requester VPC (the local VPC) and the accepter VPC, which can be in this account or another account or Region.
6. Choose **Create peering connection**.
7. The owner of the accepter VPC must accept the peering connection. Once accepted, it is active.
8. Add a route in each VPC's route table that sends the other VPC's CIDR block to the peering connection ID.
9. Update security groups and network ACLs so the traffic is allowed.

Peering is not transitive, so traffic cannot pass through a peered VPC to reach a third VPC. The CIDR blocks of the two VPCs must not overlap.

### Describe the features of AWS Lambda@Edge.

AWS Lambda@Edge runs Lambda functions in response to Amazon CloudFront events, such as viewer and origin requests and responses. You create the functions in the us-east-1 (N. Virginia) Region, and Lambda replicates them to CloudFront edge locations worldwide.

Some of the features of AWS Lambda@Edge include:

* **Low latency:** Lambda@Edge functions are executed at the edge of the AWS network, close to your users. This can reduce latency and improve performance for your users.
* **Global reach:** After you publish a function version and attach it to a CloudFront distribution, the function runs at CloudFront locations worldwide.
* **Scalability:** Lambda@Edge functions can scale automatically to meet demand. This means that your applications can handle sudden spikes in traffic without any intervention from you.

### What is AWS Fargate and how is it different from ECS?

AWS Fargate is a serverless compute engine for Docker containers. AWS ECS is a container orchestration service that helps you to deploy, manage, and scale containerized applications.

### Fargate vs. ECS

| Feature | Fargate | ECS (EC2 launch type) |
|---|---|---|
| Serverless | Yes | No |
| Container orchestration | No (runs tasks scheduled by ECS or EKS) | Yes |
| Scaling | Task count managed by ECS Service Auto Scaling; no instances to manage | Task count managed by ECS Service Auto Scaling; instance capacity managed with EC2 Auto Scaling or capacity providers |
| Pricing | Per vCPU and memory, billed per second | No ECS charge; you pay for the EC2 instances and resources |

### How does AWS Artifact enhance compliance and security?

AWS Artifact enhances compliance and security in a number of ways.

#### Compliance

* AWS Artifact provides on-demand access to AWS security and compliance reports, such as SOC and ISO reports, as well as compliance agreements. This makes it easy to find and access the documents you need when preparing for audits.
* AWS Artifact Agreements lets you review, accept, and track agreements such as the Business Associate Addendum (BAA).

#### Security

* Access to reports and agreements is controlled with AWS Identity and Access Management (IAM) policies.
* Agreement activity is logged to AWS CloudTrail, so you can audit who accepted or changed an agreement.

Examples:

* A healthcare company subject to HIPAA can accept the BAA in AWS Artifact Agreements and download AWS audit reports for its own compliance reviews.
* A payments company can download AWS's PCI DSS compliance report as evidence for its own PCI DSS assessment.

### What is AWS PrivateLink, and how does it improve network security?

AWS PrivateLink lets you connect your VPC privately to AWS services and to services that other VPCs or accounts expose, without using the public internet. PrivateLink traffic stays on the AWS network; for end-to-end protection of application payloads, use TLS or another application-level encryption.

With PrivateLink, traffic to the service does not need an internet gateway, NAT device, or public IP address.

### Explain the use of AWS Greengrass Core.

**AWS IoT Greengrass Core** is a software agent that runs on local devices and enables them to communicate with AWS cloud services. It provides local compute, messaging, data caching, and synchronization capabilities. Greengrass Core also provides security features such as encryption and authentication.

Greengrass Core can be used in a variety of ways, including:

* To run machine learning models on edge devices
* To collect and analyze data from edge devices
* To control edge devices from the cloud
* To provide local caching and synchronization for edge devices

### How do you set up AWS IAM Identity Center (formerly AWS SSO)?

To set up AWS IAM Identity Center (the successor to AWS SSO), follow these steps:

1. Enable IAM Identity Center in the management account of your organization.
2. Choose an identity source: the built-in Identity Center directory, Active Directory, or an external SAML 2.0 or OIDC identity provider.
3. Create permission sets. Each one is deployed as an IAM role in the accounts you assign it to.
4. Assign users and groups to accounts and applications with those permission sets.

Users then sign in to the AWS access portal with their Identity Center credentials.

### What is AWS Cost Explorer, and how does it help in cost analysis?

AWS Cost Explorer is a service that helps you to analyze your AWS costs. Cost Explorer provides a variety of reports and dashboards that can help you to understand your costs, identify areas where you can save money, and optimize your AWS usage.

Cost Explorer supports the following:

* **Filtering and grouping:** Break down costs by service, linked account, Region, or cost allocation tag.
* **Forecasts:** Projects future spend based on historical usage.
* **Recommendations:** Surfaces Savings Plans and Reserved Instance purchase recommendations.

### Describe the use cases for AWS Organizations.

AWS Organizations is a service that helps you to manage multiple AWS accounts in a single place. Organizations provides a centralized way to create, manage, and audit AWS accounts.

Common uses include:

* **Account structure:** Group accounts into organizational units (OUs), for example by environment or business unit.
* **Guardrails:** Apply service control policies (SCPs) to limit what accounts can do.
* **Consolidated billing:** Combine usage into one bill for all member accounts.
* **Account creation:** Create member accounts programmatically or through AWS Control Tower.

### What is the AWS CDK (Cloud Development Kit)?

AWS CDK is a software development framework that allows you to define your AWS infrastructure as code. CDK supports TypeScript, JavaScript, Python, Java, C#, and Go.

CDK apps are synthesized into CloudFormation templates. You deploy them with the CDK CLI (`cdk deploy`), and reusable building blocks are called constructs.

### How do you implement cross-account access in AWS?

There are two main ways to implement cross-account access in AWS:

1. **Cross-account IAM roles:** Principals in one account assume a role in another account. The role's trust policy must allow the source principal, and the source identity needs `sts:AssumeRole` permission for that role.
2. **Resource-based policies:** Resource-based policies allow you to specify who can access specific resources in your account. To do this, you attach a resource-based policy to the resource that you want to share.

### Explain the difference between Amazon Kinesis Data Streams and Kinesis Data Analytics.

Amazon Kinesis Data Streams is a real-time data streaming service that allows you to ingest and process streaming data from a variety of sources, such as web applications, sensors, and social media feeds. Kinesis Data Streams provides a durable and scalable platform for processing streaming data in real time.

Amazon Kinesis Data Analytics for SQL ended support on January 27, 2026. Kinesis Data Analytics for Apache Flink is now Amazon Managed Service for Apache Flink, which supports Java, Python, Scala, and SQL.

### What is AWS Snowmobile, and when is it used?

AWS Snowmobile was a petabyte-scale data transfer service that moved exabyte-scale data volumes in shipping containers. AWS retired Snowmobile in 2024; use AWS DataSync or the AWS Data Transfer Terminal for large transfers instead.

### How do you use AWS Elastic Beanstalk with Docker containers?

To use AWS Elastic Beanstalk with Docker containers, put a Dockerfile at the root of your project, run `eb init -p docker` to configure the project, and then run `eb create <environment-name>` to build and launch it. Elastic Beanstalk will automatically provision and configure the resources that you need to run your Dockerized application.

### Describe the features of AWS Control Tower.

AWS Control Tower is a service that helps you to set up and govern a secure, multi-account AWS environment. Control Tower provides a number of features to help you manage your AWS environment, including:

* **Account management:** Control Tower helps you to create and manage AWS accounts.
* **Networking:** Control Tower helps you to configure networking between your AWS accounts.
* **Security:** Control Tower helps you to implement security best practices in your AWS environment.
* **Governance:** Control Tower helps you to govern your AWS environment by providing a central place to manage your AWS policies and permissions.

### What is the AWS Partner Network (APN), and how does it support customers?

The AWS Partner Network (APN) is a global community of partners that leverage programs, expertise, and resources to build, market, and sell customer offerings. This diverse network features more than 130,000 partners from over 200 countries.

Customers work with partners for:

* **Consulting and implementation:** Partners design, build, and migrate workloads on AWS.
* **Marketplace offerings:** Partners sell software and services through AWS Marketplace.
* **Training and support:** Partners provide training and ongoing support for AWS products and services.

### How do you configure Amazon CloudFront with SSL?

To use your own domain name with HTTPS on CloudFront, attach an ACM certificate to the distribution and list the domain as an alternate domain name (CNAME). Follow these steps:

1. Request or import a certificate for your domain in AWS Certificate Manager (ACM) in the us-east-1 (N. Virginia) Region. CloudFront only accepts ACM certificates from that Region.
2. Open the Amazon CloudFront console, choose your distribution, and choose **Edit** in its settings.
3. Add your domain under **Alternate domain names (CNAMEs)**.
4. Under **Custom SSL certificate**, choose the certificate from step 1.
5. Set the **Viewer protocol policy**, for example to redirect HTTP to HTTPS, and choose a minimum TLS security policy.
6. Save the changes, then create a DNS record that points your domain to the distribution's domain name.

### Explain the AWS Elastic Transcoder service.

AWS Elastic Transcoder was a service that encoded media files for delivery across a variety of devices and platforms, supporting formats such as MP4, HLS, and MPEG-DASH. AWS discontinued Elastic Transcoder on November 13, 2025, and recommends AWS Elemental MediaConvert for transcoding workloads.
### What is AWS Transit Gateway Network Manager?

AWS Transit Gateway Network Manager (part of AWS Network Manager) helps you to manage and visualize your AWS Transit Gateway networks. It provides a number of features to help you manage your Transit Gateway networks, including:

* **Network topology visualization:** Transit Gateway Network Manager provides a graphical view of your Transit Gateway network topology. This helps you to understand how your network is connected and to identify potential problems.
* **Route analysis:** Transit Gateway Network Manager includes a Route Analyzer that helps you analyze the routes in your Transit Gateway route tables. This helps you to understand and troubleshoot the flow of traffic in your network.
* **Monitoring and alerts:** Transit Gateway Network Manager monitors your Transit Gateway network and sends you alerts if there are any problems.

### How does AWS PrivateLink work with service endpoints?

AWS PrivateLink works with interface VPC endpoints to provide a private and secure way to connect your VPC to AWS services. Interface endpoints are elastic network interfaces powered by PrivateLink that allow you to connect to AWS services without using the public internet; gateway endpoints, by contrast, use route table entries for S3 and DynamoDB.

When you create an interface endpoint, AWS places elastic network interfaces with private IP addresses in the subnets you choose. Enable private DNS on the endpoint so the service's standard hostname resolves to those addresses, which requires no application changes. Control access with the endpoint policy and with security groups on the endpoint's network interfaces.

### Describe AWS DMS (Database Migration Service) and its use cases.

AWS DMS is a service that helps you to migrate your databases to AWS. DMS supports a variety of database types, including MySQL, PostgreSQL, Oracle, and SQL Server.

DMS can be used to migrate databases for a variety of reasons, including:

* **One-time migrations:** Move a database to AWS with a full-load copy of the data.
* **Continuous replication:** Keep the target in sync with ongoing changes (change data capture) until you cut over.
* **Heterogeneous migrations:** Pair DMS with the AWS Schema Conversion Tool (SCT) to convert schemas between database engines.

DMS pricing is based on the replication instances and storage you use.

### What is AWS Chime, and how does it facilitate video conferencing?

Amazon Chime was a unified communications service that provided voice, video, messaging, and screen sharing capabilities. AWS ended support for the Amazon Chime service on February 20, 2026; the Amazon Chime SDK remains available for building custom meeting applications.

Teams that need video meetings inside their own applications can build on the Amazon Chime SDK.

### How do you use AWS Organizations to consolidate billing?

AWS Organizations allows you to consolidate billing for your AWS accounts. This can be useful for organizations that have multiple AWS accounts and want to manage their billing centrally.

To consolidate billing, create an organization from your management account and invite the other accounts. Consolidated billing is part of the all features set, which is the default when you create an organization.

Steps:

1. Sign in to the management account and open the AWS Organizations console.
2. Choose **Create organization**. All features is the default set.
3. Invite the accounts you want to include, by account ID or email address.
4. Have each invited account accept the invitation.

Once the accounts have joined the organization, their usage is combined into a single bill that you can view and download from the AWS Billing and Cost Management console.

### What is Amazon Polly, and how does it convert text to speech?

Amazon Polly is a cloud service that converts text to speech. It uses deep learning technologies to synthesize natural-sounding human speech. Polly supports a variety of languages and voices, and it can produce audio in formats such as MP3, Ogg Vorbis, and PCM; SSML can be used as input markup to control how the text is spoken.

#### How Amazon Polly converts text to speech

Amazon Polly converts text to speech by following these steps:

1. It breaks the text down into individual words and phonemes.
2. It synthesizes the phonemes into speech using a deep learning model.
3. It applies post-processing techniques, such as prosody and intonation, to make the speech sound more natural.

### Explain the concept of AWS EventBridge.

AWS EventBridge is a serverless event bus service that makes it easy to connect applications together and build event-driven applications. EventBridge delivers events to targets such as AWS Lambda functions, Amazon Kinesis Data Streams, and Amazon SNS topics.

### How to use AWS EventBridge

To use AWS EventBridge, you first need to create an event rule. An event rule specifies the event pattern that EventBridge should match. Once you have created an event rule, you need to configure one or more targets for the rule. Targets are the resources that EventBridge will send events to when the event pattern matches.

### How do you use AWS Data Pipeline for data integration?

AWS Data Pipeline helped orchestrate data-driven workflows between AWS services such as Amazon S3, Amazon Redshift, and Amazon DynamoDB, as well as on-premises systems. The service is now in maintenance mode and closed to new customers, so new workloads should use AWS Glue, Amazon MWAA, or AWS Step Functions instead.

To use AWS Data Pipeline for data integration, you first need to create a pipeline definition. A pipeline definition specifies the data sources, data destinations, and data processing steps for your pipeline. Once you have created a pipeline definition, you can start the pipeline. Data Pipeline will then start moving data between the data sources and data destinations that you specified in the pipeline definition.

### Describe the features of AWS CodeGuru

AWS CodeGuru is a service that helps you to improve the quality of your code. CodeGuru uses machine learning to analyze your code and identify potential problems, such as security vulnerabilities, performance bottlenecks, and bugs. Note that Amazon CodeGuru Reviewer closed to new customers on November 7, 2025, and Amazon CodeGuru Security ended support on November 20, 2025. For code security scanning in your IDE, AWS points to Amazon Q Developer.

#### Features of AWS CodeGuru

AWS CodeGuru provides a number of features to help you improve the quality of your code, including:

* **Code reviews:** CodeGuru automatically reviews your code and identifies potential problems.
* **Recommendations:** CodeGuru provides recommendations on how to fix potential problems in your code.
* **Insights:** CodeGuru provides insights into your code quality, such as the number of bugs and security vulnerabilities in your code.

## List of AWS services with brief description

### Compute

- **Amazon Elastic Compute Cloud (EC2):** Scalable virtual servers for running applications.
- **AWS Fargate:** Serverless compute engine for containers.
- **AWS Lambda:** Serverless compute service for running code without provisioning servers.

### Storage

- **Amazon Simple Storage Service (S3):** Object storage service for storing and retrieving data.
- **Amazon Elastic Block Store (EBS):** Block storage service for EC2 instances.
- **Amazon Elastic File System (EFS):** A fully managed, scalable file system for AWS and on-premises workloads.
- **Amazon S3 Glacier:** Low-cost archival storage classes of Amazon S3 for long-term data archiving (S3 Glacier Flexible Retrieval and S3 Glacier Deep Archive).
- **AWS Storage Gateway (S3 File Gateway):** Stores file data as objects in Amazon S3, for data lakes, backups, and ML workflows.

### Databases

- **Amazon Relational Database Service (RDS):** Managed relational database service for SQL databases.
- **Amazon Aurora:** Relational database service that is MySQL- and PostgreSQL-compatible.
- **Amazon Neptune:** Managed graph database service.
- **Amazon Timestream:** Fully managed, serverless time-series database (Timestream for LiveAnalytics closed to new customers in June 2025; see Timestream for InfluxDB).
- **Amazon Redshift:** Fully managed, petabyte-scale data warehouse that uses massively parallel processing (MPP) to run analytical queries in parallel.
- **Amazon DynamoDB:** Fully managed, serverless key-value and document database with single-digit millisecond latency at any scale.
- **Amazon DynamoDB Accelerator (DAX):** Fully managed, in-memory cache for DynamoDB that delivers up to 10x performance improvement.
- **Amazon DocumentDB:** Fully managed document database compatible with MongoDB workloads.
- **Amazon ElastiCache:** Fully managed in-memory data store and cache (Redis OSS, Valkey, and Memcached).
- **Amazon Keyspaces (for Apache Cassandra):** A scalable, highly available, and managed Apache Cassandra–compatible database service.

### Networking

- **Amazon Virtual Private Cloud (VPC):** Networking service to create isolated virtual networks.
- **AWS VPC peering:** A networking connection between two VPCs that enables you to route traffic between them privately.
- **Elastic Load Balancing (ELB):** Distributes incoming traffic across multiple targets, such as EC2 instances and containers.
- **Amazon Route 53:** Scalable and highly available Domain Name System (DNS) web service.
- **AWS Direct Connect:** A dedicated network connection from your on-premises data center to AWS.
- **AWS Transit Gateway:** Service for connecting multiple VPCs and on-premises networks.
- **AWS VPN CloudHub:** A hub-and-spoke model that connects multiple on-premises sites through a virtual private gateway over Site-to-Site VPN connections, allowing remote offices to communicate with each other and with AWS.
- **AWS Transit Gateway Peering:** A service that allows you to connect two or more AWS Transit Gateways together.
- **AWS Network Manager:** Central view and management of Transit Gateway and AWS Cloud WAN networks.
- **AWS Global Accelerator:** Improve application availability and performance using the AWS global network.
- **AWS PrivateLink:** A secure way to connect two services that are running in a virtual private cloud (VPC) or on-premises network to services running in AWS.
- **AWS Client VPN:** Managed client VPN for secure remote access to AWS and on-premises resources over an encrypted tunnel.
- **Amazon VPC Lattice:** Application networking service for connecting, securing, and monitoring service-to-service traffic across VPCs and accounts.
- **AWS VPC endpoints:** Let resources in a VPC connect to AWS services without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Interface endpoints are elastic network interfaces powered by AWS PrivateLink; gateway endpoints are route table targets for Amazon S3 and DynamoDB.

### Content Delivery

- **Amazon CloudFront:** Content delivery network (CDN) for fast content delivery.
- **Amazon CloudFront Origin Access Control (OAC):** OAC (the successor to Origin Access Identity) restricts access to an Amazon S3 origin so that content can only be served through the associated CloudFront distribution.
- **Amazon CloudFront Signed URL:** A URL signed with a CloudFront key pair or trusted key group, used to restrict access to specific objects.
- **CloudFront Function:** A lightweight, JavaScript-only edge function that can modify or filter content at CloudFront edge locations; distinct from Lambda@Edge, which runs full Lambda functions.
- **Amazon CloudFront Distribution:** The configuration that serves content to viewers through one or more origins, such as Amazon S3 buckets or Amazon EC2 instances.
- **Amazon CloudFront Edge Location:** Points of presence worldwide that cache content and serve viewers with low latency.

### Messaging

- **Amazon Simple Notification Service (SNS):** Pub/sub messaging service for sending messages and notifications.
- **Amazon Pinpoint:** A multichannel messaging service for engaging customers across SMS, email, push notifications, and in-app messages. AWS closed Pinpoint to new customers in May 2025, and its engagement features reached end of support on October 30, 2026 (replacements include AWS End User Messaging, Amazon SES, and Amazon Connect).

### Queuing

- **Amazon Simple Queue Service (SQS):** A fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.
- **Amazon Simple Workflow Service (SWF):** A fully managed workflow coordination service that makes it easy to build applications that coordinate work across distributed components.
- **Amazon MQ:** Managed message broker service, supports Apache ActiveMQ and RabbitMQ.
- **Amazon Managed Streaming for Apache Kafka (MSK):** A fully managed service that makes it easy to run, manage, and scale Apache Kafka clusters on AWS.

### Machine Learning and AI

- **Amazon Bedrock:** Fully managed service for building generative AI applications with foundation models through a single API.
- **Amazon SageMaker AI (formerly Amazon SageMaker):** Fully managed service to build, train, and deploy machine learning models.
- **Amazon Rekognition:** Image and video analysis service for object detection and recognition.
- **Amazon Polly:** Text-to-speech service.
- **Amazon Comprehend:** Natural language processing service for text analysis.
- **Amazon Translate:** Language translation service.
- **Amazon Transcribe:** Automatic speech recognition service.
- **Amazon Comprehend Medical:** Natural language processing for medical text.
- **Amazon CodeGuru:** AI service for code reviews and application performance recommendations (CodeGuru Security reached end of support November 20, 2025).
- **Amazon Lookout for Vision:** Find defects in images using computer vision (end of support October 31, 2025).
- **Amazon Lookout for Equipment:** Detect abnormal equipment behavior using machine learning (end of support October 7, 2026).
- **Amazon Lookout for Metrics:** Find anomalies in metrics using machine learning (end of support October 2025).
- **Amazon Fraud Detector:** Detects fraud with machine learning models built on transaction history, customer demographics, and device information (closed to new customers November 7, 2025).
- **Amazon Personalize:** A machine learning service that helps you create personalized experiences for your customers.
- **Amazon Kendra:** A cloud-based enterprise search service that uses machine learning to index and search all of your enterprise content.
- **Amazon SageMaker Canvas:** Quickly build, train, and deploy machine learning models without writing code.
- **AWS Panorama:** Build and deploy computer vision applications on edge appliances (closed to new customers; end of support May 20, 2026).

### Chat and Conversational Interfaces

- **Amazon Lex:** Chatbot and conversational interface service.

### Developer Tools

- **AWS CodePipeline:** Continuous integration and continuous delivery (CI/CD) service.
- **AWS CodeBuild:** A fully managed continuous integration (CI) service that compiles source code, runs tests, and produces software packages that are ready to deploy.
- **AWS CodeDeploy:** Deployment service for applications on Amazon EC2, on-premises servers, AWS Lambda, and Amazon ECS.
- **AWS CloudFormation:** Infrastructure as Code service for provisioning AWS resources.
- **AWS Cloud9:** Cloud-based integrated development environment (IDE) (closed to new customers in July 2024).
- **AWS Cloud Development Kit (CDK):** An open-source software development framework to model and provision your cloud application resources using familiar programming languages.
- **AWS Serverless Application Model (SAM):** An open-source framework that makes it easy to build, deploy, and manage serverless applications on AWS. SAM applications are made up of AWS Lambda functions, Amazon API Gateway APIs, and other AWS resources.
- **AWS SDK:** A collection of software development kits (SDKs) that you can use to access and manage AWS services (for a variety of programming languages).
- **AWS Amplify:** A collection of tools and services that makes it easy to develop mobile and web applications.
- **AWS Lightsail:** A service that makes it easy to deploy and manage websites and web applications and offers a variety of pre-configured virtual machines (VMs) with different levels of resources.
- **AWS AppSync:** A fully managed service that makes it easy to build serverless, real-time applications (GraphQL API).

### Management and Monitoring

- **Amazon CloudWatch:** A monitoring and observability service that collects logs, metrics, and events to provide data and actionable insights to help you monitor your applications, infrastructure, and services.
- **Amazon CloudTrail:** A service that helps you track and audit user activity and API usage across your AWS resources.
- **AWS Systems Manager:** A collection of services and features that helps automate management of your AWS resources, including patch management, configuration management, fleet inventory, run command, and maintenance window.
- **AWS OpsWorks:** Managed Chef Automate and Puppet Enterprise servers, both end of life on May 1, 2024; AWS recommends migrating to Chef SaaS or another alternative.
- **AWS Config:** Configuration management service for assessing, auditing, and evaluating resources.
- **AWS Systems Manager Automation:** Service for automating operational tasks.
- **AWS Systems Manager Patch Manager:** Automate patch management for your instances.
- **AWS CloudWatch Synthetics:** Service for testing application endpoints.
- **Amazon DevOps Guru:** ML-powered service to improve application availability.
- **AWS Control Tower:** A managed service that helps you set up and govern a secure, multi-account AWS environment.

### Security and Compliance

- **AWS Identity and Access Management (IAM):** Control who can access AWS services and resources, through users, roles, and policies.
- **AWS IAM Identity Center:** Centrally manage workforce access to multiple AWS accounts and business applications (formerly AWS Single Sign-On).
- **AWS Secrets Manager:** Store, rotate, and retrieve database credentials, API keys, and other secrets.
- **Amazon GuardDuty:** Uses machine learning to continuously monitor AWS accounts and workloads for malicious activity and unauthorized behavior.
- **AWS Audit Manager:** Service for simplifying and automating compliance audits.
- **AWS Security Hub:** A cloud security posture management service that provides a comprehensive view of your security posture across your AWS accounts and Regions.
- **AWS Shield:** Managed Distributed Denial of Service (DDoS) protection.
- **AWS WAF:** Web Application Firewall for protecting web applications.
- **AWS Firewall Manager:** Central management for AWS WAF and AWS Shield.
- **AWS Network Firewall:** Managed firewall service.
- **Amazon Macie:** Discover, classify, and protect sensitive data using ML.

### Orchestration and Integration

- **Amazon EventBridge:** Serverless event bus for connecting applications.
- **AWS Step Functions:** Serverless orchestration service for coordinating distributed applications.
- **Amazon Simple Email Service (SES):** Email sending and receiving service.
- **Amazon API Gateway:** Fully managed service for creating and managing APIs.

### Containers and Kubernetes

- **Amazon Elastic Container Service (ECS):** Container orchestration service.
- **Amazon Elastic Kubernetes Service (EKS):** Managed Kubernetes service for container orchestration.
- **Amazon EKS Anywhere:** Run Kubernetes clusters on your own infrastructure.
- **Amazon EKS with Fargate:** Run Kubernetes pods on serverless Fargate compute.
- **AWS App Runner:** Service for building and running containerized applications (no longer open to new customers; Amazon ECS Express Mode is the suggested path).
- **AWS App Mesh:** Service mesh for microservices (reached end of support September 30, 2026; use Amazon ECS Service Connect for ECS or Amazon VPC Lattice for EKS).
- **AWS Fargate Spot:** Fargate capacity option that runs interruptible tasks on spare capacity at a lower price.
- **Amazon Elastic Container Registry (ECR):** Fully managed Docker container registry.

### Data Services

- **AWS Data Pipeline:** Service for moving data between different AWS services (closed to new customers; AWS recommends other data integration services).
- **Amazon Lake Formation:** Service to set up and manage a data lake.
- **AWS Lake Formation Permissions:** Manage permissions in AWS Lake Formation.
- **AWS Lake Formation Governed Tables:** Tables in AWS Lake Formation.
- **AWS Lake Formation Analytics:** Analyze data in AWS Lake Formation.
- **AWS Glue:** ETL (Extract, Transform, Load) service for data preparation.
- **AWS Glue Data Catalog:** Managed metadata repository.
- **AWS Glue Data Catalog Serverless:** Serverless data catalog service.
- **AWS Glue Workflows:** Service for building ETL workflows.
- **AWS Glue Studio:** Visual interface for building ETL jobs.
- **Amazon Athena:** Interactive query service for data analysis.
- **Amazon Athena Federated Queries API Version 2:** API for Amazon Athena, a serverless query service that allows you to query data in Amazon S3 using SQL.
- **Amazon Redshift Spectrum External Table:** A feature of Amazon Redshift that allows you to query data in Amazon S3 using external tables.
- **AWS DataSync:** A hybrid cloud transfer service that makes it easy to automate data transfers between on-premises storage and AWS storage services.

### Internet of Things (IoT)

- **AWS IoT Core:** Internet of Things (IoT) service for connecting devices.
- **AWS IoT Device Gateway:** Gateway for IoT devices to connect to AWS.
- **AWS IoT Analytics:** Service for processing, storing, and analyzing IoT data (closed to new customers; end of support December 15, 2025).
- **AWS IoT Greengrass:** Edge computing service for IoT devices (Greengrass V1 reached end of support October 7, 2026; use Greengrass V2).
- **AWS IoT FleetWise:** Fleet management for IoT devices.
- **AWS IoT Edge:** Extend AWS IoT to edge devices for IoT applications.
- **AWS IoT FleetWise Edge:** Manage IoT device fleets at the edge.
- **AWS IoT SiteWise Edge:** Process IoT data locally at the edge.
- **AWS IoT TwinMaker Edge:** Create digital twins at the edge.
- **Amazon Monitron:** Monitoring of industrial equipment with sensors and machine learning (closed to new customers October 31, 2024).
- **AWS IoT Analytics Transfer for Apache Kafka:** Transfer data to and from Apache Kafka.
- **AWS IoT Events:** Detect and respond to IoT events (end of support May 20, 2026).

### Hybrid Cloud and Edge Computing

- **AWS Outposts:** Extend AWS infrastructure and services to your data center.
- **AWS Wavelength:** Deploy applications that require ultra low latency to mobile devices.
- **AWS Local Zones:** AWS infrastructure and services close to large population centers.
- **AWS Snow Family:** Physically transport large amounts of data into and out of AWS. Snowcone was discontinued (November 12, 2024), and Snowball Edge is no longer available to new customers.

### Operations

- **AWS Artifact:** A self-service portal for on-demand access to AWS compliance reports and agreements, such as SOC and ISO reports and the HIPAA business associate agreement.
- **AWS Trusted Advisor:** An online service that scans your environment and gives real-time recommendations across cost optimization, performance, security, fault tolerance, and service limits.
- **AWS Well-Architected Tool:** Review and improve your cloud architectures.
- **AWS Resilience Hub:** Prepare your business for disruptions and uncertainties.

### Governance and Compliance

- **AWS Organizations:** Centrally manage multiple AWS accounts.
- **AWS Key Management Service (KMS):** Managed service for creating and controlling encryption keys.
- **AWS CloudHSM:** A cloud-based hardware security module (HSM) that enables you to generate and store cryptographic keys in the cloud.

### Blockchain

- **Amazon Managed Blockchain:** Create and manage scalable blockchain networks (closed to new customers October 29, 2026; end of support September 29, 2027).
- **Amazon Quantum Ledger Database (QLDB):** A fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log (end of support July 31, 2025; Amazon Aurora PostgreSQL is the suggested replacement).

### Satellite

- **AWS Ground Station:** Fully managed ground station as a service.

### Robotics

- **AWS RoboMaker:** Develop, simulate, and deploy robotics apps (end of support September 10, 2025).

### Quantum Computing

- **Amazon Braket:** Explore and experiment with quantum computing.

### Analytics & Big Data

- **Amazon OpenSearch Service:** Managed service for deploying and operating OpenSearch and OpenSearch Dashboards (formerly Amazon Elasticsearch Service).
- **Amazon Kinesis:** Real-time data streaming service for ingesting and processing large streams of data.
- **Amazon Kinesis Data Streams:** A real-time data streaming service that can process millions of records per second.
- **Amazon Data Firehose:** A fully managed service that delivers real-time streaming data to Amazon S3, Amazon Redshift, Amazon OpenSearch Service, Splunk, and supported HTTP endpoints (formerly Amazon Kinesis Data Firehose).
- **Amazon EMR:** Managed cluster platform for Apache Spark, Hadoop, and other big data frameworks.

### Customer Engagement

- **Amazon Connect:** An omnichannel cloud contact center service that makes it easy to set up, manage, and scale your contact center.

### End User Computing

- **Amazon WorkSpaces:** Managed, secure cloud desktops for users.
- **Amazon WorkSpaces Applications (formerly Amazon AppStream 2.0):** Fully managed application streaming service that delivers apps to users on any device.

### Management Tools

- **AWS Service Catalog:** Create, manage, and share catalogs of approved, standardized IT products for end users.
- **AWS License Manager:** A service that helps you manage your software licenses across your AWS resources.
- **AWS Systems Manager Parameter Store:** Store and retrieve configuration data.

### Media Services

- **Amazon Kinesis Video Streams:** Process and analyze video streams.

### Migration

- **AWS Migration Hub:** A service that helps you plan, migrate, and manage your migrations to AWS.
- **AWS Application Discovery Service (ADS):** Discovers applications running on-premises and collects data about their dependencies, relationships, and usage patterns.
- **Amazon Database Migration Service (DMS):** A service that helps you migrate databases from on-premises to AWS or from one AWS database service to another.
- **AWS Application Migration Service (MGN):** Lift-and-shift applications to AWS with minimal downtime.
- **AWS Server Migration Service (SMS):** AWS ended support for SMS on April 1, 2023; its successor, AWS Application Migration Service (MGN, now AWS Transform MGN), automates lift-and-shift migrations with minimal downtime.

## Microsoft Azure

### 1. What is Microsoft Azure, and how does it work?

Microsoft Azure is a cloud computing platform that provides a wide range of services, like storage, computing, and databases, hosted in Microsoft data centers. It lets businesses build, deploy, and manage applications globally, using tools and frameworks of their choice.

### 2. Explain the core services provided by Azure.

Azure provides core services like Compute, which includes virtual machines and containers; Storage for data solutions like Blob and Disk Storage; Networking to manage connectivity with services like Virtual Network; and Databases including SQL Database and Cosmos DB.

### 3. What is Azure Resource Manager (ARM)?

Azure Resource Manager (ARM) is the deployment and management layer for Azure, exposed as a RESTful API. It organizes resources into resource groups, applies role-based access control (RBAC), and manages resources through templates. Because management requests go through ARM, deployments can be automated and repeated consistently.

### 4. Describe the differences between Azure IaaS, PaaS, and SaaS.

The three service models differ in how much of the stack Azure manages and how much you manage yourself:

- **IaaS (Infrastructure as a Service)**: Virtualized infrastructure such as VMs, storage, and networks. You manage the OS, runtime, applications, and data. Example: Azure Virtual Machines, where you handle OS updates and configuration.
- **PaaS (Platform as a Service)**: A managed platform to develop, run, and manage applications. You focus on your application and data, while Azure manages the OS, runtime, and infrastructure. Example: Azure App Service.
- **SaaS (Software as a Service)**: Fully managed software delivered over the internet. You use the application and manage only your data, users, and configuration. Example: Microsoft 365.

As you move from IaaS to SaaS, Azure takes on more of the management responsibility.

### 5. How does Azure Virtual Network work, and what are its components?

Azure Virtual Network (VNet) is a private, isolated network in Azure that lets resources communicate securely with each other, the internet, and on-premises networks. Its main components are:

- **Address space and subnets**: A CIDR address range for the VNet, divided into subnets to segment resources.
- **Network security groups (NSGs)**: Filter inbound and outbound traffic using rules applied to subnets or network interfaces.
- **VNet peering**: Links VNets in the same or different regions.
- **VPN Gateway and ExpressRoute**: Connect the VNet to on-premises networks through site-to-site or point-to-site VPN, or a private ExpressRoute connection.
- **Route tables (UDRs)**: Override Azure's default routing to control how traffic flows.
- **Service endpoints and Private Link**: Provide private access to PaaS services such as Storage and SQL Database.
- **DNS**: Name resolution through Azure-provided DNS or custom DNS servers.

### 6. What is Microsoft Entra ID (formerly Azure Active Directory), and how is it used?

Microsoft Entra ID (formerly Azure Active Directory, renamed in 2023) is Microsoft's cloud-based identity and access management service. It is used for:

- **Authentication**: User sign-in, single sign-on (SSO), and multifactor authentication (MFA).
- **Conditional Access**: Policies that allow or block access based on user, device, location, and risk signals.
- **Access management**: Role- and group-based access to Azure resources and applications, managed through app registrations and enterprise applications.
- **Device identity**: Joining and registering devices to Entra ID, with device management through Microsoft Intune.
- **Integration**: Built into Microsoft 365, Azure, and thousands of SaaS applications.
- **External identities**: Collaboration with partner users (B2B) and customer sign-in through Microsoft Entra External ID, which is the successor to Azure AD B2C for new customers.

7. Explain Azure App Service and its use cases.
8. How does Azure Storage work, and what are its types?
9. Describe Azure SQL Database and its features.
10. What is Azure Functions, and how does serverless computing work in Azure?
11. How do you ensure data redundancy and disaster recovery in Azure?
12. Explain the role of Azure DevOps in application development.
13. What is Azure Kubernetes Service (AKS), and how does container orchestration work in Azure?
14. Describe Azure Cosmos DB and its global distribution features.
15. How do you optimize costs in Azure?
16. What is Azure Logic Apps, and how are workflows created?
17. Explain the concept of Microsoft Defender for Cloud (formerly Azure Security Center) and its role in security management.
18. How do you implement high availability in Azure?
19. What is Azure CDN (Content Delivery Network), and how does it compare with Azure Front Door? Azure CDN from Microsoft (classic) retires September 30, 2027.
20. Describe the benefits of Azure Functions for event-driven applications.
21. How does Azure Monitor (including its Log Analytics feature) work for cloud monitoring?
22. What is Azure ExpressRoute, and how does it enable private network connections?
23. Explain Azure Machine Learning and its applications.
24. How do you secure data in Azure Storage and databases?
25. What is Azure Application Gateway, and how does it improve application delivery?
26. Describe the Azure Resource Manager template (ARM template).
27. How do you migrate on-premises workloads to Azure?
28. What is Azure Key Vault, and how does it manage secrets and keys?
29. Explain the concept of Azure Policy and governance.
30. What is Azure Data Factory, and how is it used for data integration?
31. How does Azure Virtual WAN enhance network connectivity?
32. Describe Azure API Management and its role in API governance.
33. What is Azure Data Lake Storage, and how does it handle big data?
34. How do you set up Microsoft Entra ID for single sign-on (SSO)?
35. What is Azure Synapse Analytics, and how does it enable analytics at scale?
36. Explain the features of Azure Event Grid for event-driven architectures.
37. How do you manage Azure resources using Azure PowerShell?
38. What is Azure Firewall, and how does it enhance network security?
39. Describe the use of Azure Blueprints for governance and compliance, and what replaces it (Azure Blueprints retires January 31, 2027).
40. What is Azure IoT Hub, and how does it enable IoT device communication?
41. What is Azure Service Bus, and how does it facilitate messaging?
42. Explain the Azure Container Registry (ACR) for container image storage.
43. What is Azure Bastion, and how does it secure remote access?
44. What is Azure Arc, and how does it extend Azure services to on-premises and multi-cloud environments?
45. Explain the concept of Durable Functions in Azure.
46. How do you ensure data encryption in Azure services?
47. What is Azure Private Link, and how does it enhance security?
48. Describe the use of Azure Stream Analytics for real-time data processing.
49. How do you monitor application performance with Azure Application Insights?
50. What are Foundry Tools (formerly Azure AI services and Azure Cognitive Services), and how do they enable AI capabilities?
51. Explain Azure DevTest Labs and its use for development and testing.
52. How do you achieve cross-region and cross-cloud redundancy in Azure?
53. What is Azure Front Door, and how does it optimize global application delivery?
54. Describe the use of Azure Logic Apps and Power Automate for workflow automation.
55. How do you use Microsoft Entra External ID for B2B collaboration and customer identity?
56. What is Azure Backup, and how does it work for data protection?
57. Explain Azure Confidential Computing and its security benefits.
58. How do you set up Microsoft Entra ID multi-factor authentication (MFA)?
59. What is Azure Quantum, and how does it enable quantum computing solutions?
60. Describe the benefits of Azure Local (formerly Azure Stack HCI) and Azure Stack Hub for hybrid cloud deployments.
61. How does Azure Data Explorer (ADX) enable data exploration and analysis?
62. What is Azure Firewall Manager, and how does it enhance network security management?
63. Explain Azure Time Series Insights (retired July 2024) for IoT data analysis.
64. How do you manage Azure resources using Azure CLI?
65. What is Azure Lighthouse, and how does it facilitate cross-tenant management?
66. Describe the use of Azure SignalR Service for real-time communication.
67. How do you secure data transfer in Azure services?
68. What is Azure Sphere OS, and how does it protect IoT devices?
69. How does Azure Backup Center simplify backup management?
70. What is Azure Databricks, and how does it enable big data analytics?
71. Describe the use of Azure Virtual Desktop for virtualized Windows environments.
72. How do you design a resilient Azure architecture?
73. What is Azure Container Instances (ACI), and how does it simplify container deployment?
74. Explain Azure Queue Storage and its role in messaging.
75. What are rule sets in Azure Front Door Standard and Premium (the classic Rules Engine is available only in Front Door classic), and how do they enhance routing and security?
76. Describe the benefits of Azure Arc-enabled Kubernetes for hybrid cloud management.
77. Explain Azure IoT Edge for deploying AI and custom logic to edge devices.
78. What is Azure Sphere Security Service, and how does it secure IoT devices?
79. Describe the use of Azure Automation for process and configuration management.
80. How do you configure Azure Private DNS for name resolution?
81. What is Azure Migrate, and how does it simplify migration to Azure?
82. Explain Azure Functions Premium Plan and its scalability features.
83. How do you achieve compliance in Azure with built-in policies?
84. What is Azure Stream Analytics on IoT Edge, and how does it enable real-time analytics at the edge?
85. Describe the benefits of Azure AI Search (formerly Azure Cognitive Search) for search over your own content.
86. How do you handle data replication in Azure services?
87. What is Azure Sphere Guardian Module, and how does it enhance IoT security?
88. Explain Azure Cost Management and Billing for cost analysis.
89. How do you secure virtual machines (VMs) in Azure?
90. What is Azure IoT Central, and how does it simplify IoT solutions? It retires September 20, 2029; Azure IoT Hub and Device Provisioning Service are the recommended replacement.
91. Describe the use of Azure CycleCloud for HPC (High-Performance Computing) workloads.
92. What are Azure Virtual Machines, and how do you choose a VM size and pricing model?
93. How does Azure Load Balancer differ from Application Gateway and Azure Front Door?
94. What is Bicep, and how does it compare with ARM templates?

## Google Cloud Platform (GCP)

1. What is Google Cloud Platform (GCP), and how does it work?
2. Explain the core services provided by GCP.
3. What is Google Cloud Identity and Access Management (IAM)?
4. Describe the differences between GCP's IaaS, PaaS, and SaaS offerings.
5. How does Google Compute Engine (GCE) work, and what are its components?
6. What is Google Kubernetes Engine (GKE), and how does container orchestration work in GCP?
7. Explain the concept of Google Cloud Storage and its various storage classes.
8. How do you ensure data redundancy and disaster recovery in GCP?
9. What is Google Cloud Functions (now Cloud Run functions), and how does serverless computing work in GCP?
10. How do you optimize costs in GCP?
11. Describe how Infrastructure Manager and Terraform replace Google Cloud Deployment Manager (end of support March 31, 2026) for infrastructure as code (IaC).
12. What is Google Cloud Pub/Sub, and how does it facilitate event-driven architectures?
13. Explain the use of Google Cloud Bigtable for NoSQL data storage.
14. How does Google Cloud Load Balancing work, and what are the types of load balancers in GCP?
15. What is Google Cloud Vision API, and how does it enable image recognition?
16. Describe the benefits of Google Cloud SQL for managed relational databases.
17. How do you implement high availability in GCP?
18. What is Google Cloud CDN (Content Delivery Network), and when is it used?
19. Explain the concept of Google Cloud Security Command Center and its role in security.
20. How do you set up Google Cloud Identity-Aware Proxy (IAP) for securing applications?
21. What is Google Cloud AutoML (now Agent Platform AutoML, formerly Vertex AI AutoML), and how does it enable machine learning for non-experts?
22. Describe the use of Google Cloud Datastore (now Firestore in Datastore mode) for NoSQL data storage.
23. How does Google Cloud Monitoring and Google Cloud Logging work for cloud monitoring?
24. What is Google Cloud VPN (HA VPN is recommended; Classic VPN no longer accepts new BGP tunnels), and how does it facilitate secure connectivity?
25. Explain Google Cloud Spanner and its features for distributed databases.
26. How do you secure data in Google Cloud Storage and Google Cloud SQL?
27. What is Google Cloud Run, and how does it enable containerized applications?
28. Describe the concept of Vertex AI Workbench (now Gemini Enterprise Agent Platform Workbench; formerly Cloud Datalab) for data exploration and analysis.
29. How does Google Cloud Composer work for managing workflows?
30. What is Google Cloud Filestore, and how does it provide file storage?
31. How do you set up Access Context Manager access levels for VPC Service Controls?
32. What is Google Cloud Memorystore, and how does it provide in-memory data storage?
33. Describe the role of Identity Platform (formerly Google Cloud Identity Platform) for identity management.
34. How do you handle data backup and recovery in GCP?
35. What is Google Cloud Armor, and how does it protect web applications?
36. Explain the concept of Google Cloud Healthcare API for healthcare data management.
37. How do you use Google Cloud Endpoints for creating, deploying, and managing APIs?
38. Google Cloud IoT Core was retired in August 2023 - what are the options for IoT device management on GCP today?
39. Describe the benefits of Google Cloud Firestore for NoSQL document databases.
40. How do you achieve data encryption in Google Cloud services?
41. What is Google Cloud Service Catalog (formerly Private Catalog), and how does it help manage and distribute software catalogs?
42. What is Google Cloud Dataprep by Trifacta, and how does it assist in data preparation?
43. Describe the use of Google Cloud Build for continuous integration and continuous delivery (CI/CD).
44. How does Google Cloud Scheduler enable cron job scheduling in GCP?
45. Explain the principles of Google Cloud VPC (Virtual Private Cloud) and network connectivity.
46. How do you use Google Cloud Natural Language API for text analysis and language understanding?
47. Describe the benefits of Google Cloud Video Intelligence for video content analysis.
48. What is Google Cloud Dataflow, and how does it enable real-time and batch data processing?
49. Explain the concept of Web Security Scanner in Security Command Center for web application security.
50. How do you secure Google Cloud Endpoints for API protection?
51. Google Cloud IoT Edge was retired alongside IoT Core in August 2023 - how would you extend cloud capabilities to edge devices on GCP today?
52. Describe the use of Gemini Enterprise Agent Platform (formerly Vertex AI, earlier AI Platform) for machine learning model development.
53. What is Google Cloud Tasks, and how does it facilitate the handling of asynchronous tasks?
54. How do you achieve data replication and synchronization in GCP?
55. What is Google Cloud Data Loss Prevention (DLP, now Sensitive Data Protection), and how does it protect sensitive data?
56. Describe the benefits of Google Cloud Text-to-Speech for converting text into natural-sounding speech.
57. How does Google Cloud Data Fusion support data integration?
58. What is Google Cloud Speech-to-Text, and how does it convert spoken language into text?
59. Explain the use of Looker Studio (formerly Google Data Studio) for data visualization and reporting.
60. How do you ensure data privacy and compliance in GCP?
61. What is Google Cloud Storage Transfer Service, and how does it enable data transfer to GCP?
62. Describe the use of Google Cloud KMS (Key Management Service) for encryption key management.
63. How do you handle data archiving and retention in GCP?
64. Describe the use of Google Cloud Dialogflow for building conversational interfaces.
65. How do you use Google Cloud IAM Roles to manage permissions and access control?
66. What is Google Cloud App Engine, and how does it enable application deployment and scaling?
67. How does Google Cloud Security Health Analytics identify security vulnerabilities?
68. What is Google Cloud Network Service Tiers, and how do they optimize network performance?
69. How do you secure access to Google Cloud resources using service accounts?
70. What is Knowledge Catalog (formerly Dataplex Universal Catalog, which succeeded Google Cloud Data Catalog), and how does it facilitate metadata management?
71. What is Google Cloud Apigee, and how does it provide API management?
72. Describe the use of Google Cloud Resource Manager for organization and project management.
73. How do you ensure data integrity in Google Cloud Storage and databases?
74. What is BigQuery, and how does it differ from Cloud SQL and Bigtable for analytics workloads?
75. What is Artifact Registry, and how does it replace Container Registry?
76. What is Cloud DNS, and how do public and private managed zones differ?
## Contributing to This Repository

We welcome contributions from the community. If you have any suggestions for new topics or answers, please feel free to open an issue or submit a pull request. See [CONTRIBUTING.md](CONTRIBUTING.md) for the guidelines.

## License

The content of this handbook is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). See [LICENSE](LICENSE).

Copyright 2026 Stanislav
