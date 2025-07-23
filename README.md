```
Resilient and Scalable Web Application on AWS

This project demonstrates the implementation of a **highly available**, **scalable**, and **secure** web application infrastructure on AWS, as part of the CloudFolks HUB Capstone Program.

## 📌 Objectives
- **High Availability**: Multi-AZ deployment to reduce downtime.
- **Scalability**: Auto Scaling to handle dynamic workloads.
- **Security**: Strict IAM roles, Security Groups, and encrypted data.
- **Resilience**: Fault-tolerant architecture to withstand failures and spikes.

## 🏗️ Architecture Overview
The application architecture is built on the following AWS components:

- **VPC**: Custom Virtual Network with public and private subnets in multiple AZs.
- **EC2 Instances**: Hosts the web application.
- **Elastic File System (EFS)**: Shared, scalable storage mounted on EC2.
- **Application Load Balancer (ALB)**: Distributes traffic across instances.
- **Auto Scaling**: Automatically adjusts capacity based on traffic.
- **Route 53**: DNS management and health checks for high availability.
- **CloudWatch**: Monitoring and logging.
- **IAM**: Role-based access control for secure communication.

## ⚙️ Deployment Strategy

1. **VPC Setup**
   - Created 4 subnets (2 public, 2 private) across 2 Availability Zones.
   - Configured Internet Gateway, NAT Gateway, and custom route tables.

2. **Compute & Storage**
   - Launched EC2 instances with Auto Scaling Group.
   - Mounted EFS across EC2s for shared storage needs.

3. **Networking**
   - Configured ALB with listeners and target groups.
   - Set up Route 53 for domain routing and failover.

4. **Security**
   - Defined Security Groups for EC2, ALB, and EFS.
   - Applied IAM roles to control EC2 access and service permissions.

5. **Monitoring & Logging**
   - Enabled metrics and alerts via CloudWatch.
   - Centralized logs from EC2 and ALB.

## 📊 Performance & Optimization Summary

- **Load Testing**: Conducted simulated traffic tests to ensure stability.
- **Initial Optimization**: Improved load times and CPU utilization.
- **Iterative Improvements**: Monitored real-time usage to adjust Auto Scaling policies.
- **Cost Efficiency**: Leveraged spot instances and right-sized EC2 types.

## 🔐 Security & Compliance

- Encrypted data at rest (EFS) and in transit (TLS).
- IAM roles for least-privilege access.
- Regular security audits and compliance checks.

## 🧪 Challenges & Solutions

| Challenge                         | Solution Implemented                             |
|----------------------------------|---------------------------------------------------|
| High latency in private subnets  | Introduced NAT Gateway with optimized routing    |
| Scalability under burst traffic  | Adjusted Auto Scaling policies with buffer limits|
| Initial bootstrapping issues     | Refined EC2 user data scripts                    |

## 📁 Folder Structure
```

📦project-root
┣ 📂scripts
┣ 📂configs
┣ 📂diagrams
┣ 📜README.md
┣ 📜deployment-guide.pdf
┣ 📜architecture.pdf
┣ 📜performance-report.pdf

```
**Developed under CloudFolks HUB Capstone Project-1**  
```
