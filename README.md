# Hub-spoke-Architecture

Business Case:
As O3M expanded, their existing infrastructure became inadequate, leading to inefficiencies and operational complexities. The organization required a scalable, cost-effective, and secure solution to sustain its growth and enhance client satisfaction.

Key Challenges:
Scalability Limitations: The infrastructure struggled to accommodate the rising client demands, resulting in potential service disruptions.
Performance Bottlenecks: Slow response times and frequent downtimes negatively impacted both service delivery and internal operations.
Security Concerns: With an influx of sensitive data, robust security measures were essential to ensure data protection and regulatory compliance.
Solution Overview:
Scalability: I designed and implemented a hub-and-spoke architecture, allowing for independent scaling of each spoke based on workload requirements. This architecture provided the necessary flexibility to dynamically adjust to departmental needs.

Performance Optimization: To enhance performance, I integrated a load balancer with Virtual Machine Scale Sets (VMSS) to efficiently distribute traffic across multiple instances. I also introduced caching mechanisms to improve response times and optimized database queries and application code for increased efficiency.

Security Enhancements: Security was a paramount consideration in this project. I deployed firewalls and network security groups to manage traffic flow and prevent unauthorized access. All sensitive data was encrypted both in transit and at rest, ensuring compliance with industry standards.

Client Requirements Fulfillment:

Website Hosting: O3M’s static website was hosted on Azure App Service, enabling automated scaling based on traffic demands, complemented by automated backups to Azure Storage for resilience.
Media Delivery: To ensure reliable and fast media delivery, photos and videos were hosted on Azure Blob Storage, minimizing the load on web servers.
Secure File Access: I implemented Azure File Share with a private endpoint, facilitating secure file access for employees within the VNet.
Internal Systems: O3M’s internal systems were hosted on VMSS, interconnected with a SQL database for effective data management. The secure connection between the internal system and the database safeguarded sensitive business information while the load balancer enhanced performance.
