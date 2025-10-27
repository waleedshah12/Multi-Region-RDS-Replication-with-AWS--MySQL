🌍 Multi-Region RDS Replication with AWS (MySQL)

A hands-on cloud engineering project demonstrating cross-region RDS replication using Amazon RDS for MySQL. Designed for high availability, disaster recovery, and performance testing across geographically distributed environments.

📐 Architecture Diagram

[US Region]                        [Ireland Region]
+-------------+                   +----------------+
| RDS Primary |  <-- Replicates --| RDS Read Replica|
+-------------+                   +----------------+
      |                                   |
+-------------+                   +----------------+
| EC2 Instance|                   | EC2 Instance    |
+-------------+                   +----------------+
      |                                   |
  Custom VPC                         Custom VPC
  Private Subnet                     Private Subnet
  Security Groups                    Security Groups

  🧱 Project Components
  
• 	Primary RDS (MySQL) in US region
• 	Read Replica in Ireland region
• 	EC2 Instances in both regions for connectivity and SQL testing
• 	Custom Networking: VPCs, subnets, route tables, security groups
• 	IAM Roles for secure access and replication permissions

⚙️ Key Features

• 	✅ Cross-region replication with read-only enforcement
• 	✅ SQL-based replication validation from EC2
• 	✅ Replica lag monitoring
• 	✅ Secure, isolated networking
• 	✅ Disaster recovery readiness

🧪 Testing & Validation

• 	Verified replication using  and custom SQL queries
• 	Confirmed read-only mode on replica
• 	Monitored replication lag and performance metrics
• 	Simulated failover scenarios for DR validation

📚 Lessons Learned

• 	VPC peering, DNS resolution, and SG rules are critical for cross-region setups
• 	EC2-based SQL testing is essential for real-world validation
• 	Network latency and design directly impact replication performance

🚀 Outcome

A fully functional, secure, and scalable cross-region RDS replication setup — ready for production-grade disaster recovery and global read scalability.
