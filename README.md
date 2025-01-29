   ---
# 🌐 Cloud Migration Project: On-Premises to AWS
---
## 📋 Overview

This project demonstrates the migration of an **on-premises web application** and its associated **database** to AWS, leveraging services like **AWS DMS**, **Client VPN**, and **RDS**. The migration ensures secure connectivity, seamless data transfer, and improved scalability and availability in the cloud environment.

---
## Architecture
![alt text](<diagrams/AWS Blogs-ApplicationDiscovery-Services1200 X 644.gif>)


## 📑 Project Index & Key Documents

🔹 **[Phase 1: AWS Application Discovery & TCO Analysis](https://github.com/prafulpatel16/mgn-aws-project01/blob/master/migration/A-Phase%201-AWS%20Application%20Discovery%20%26%20TCO%20Analysis)**
   - 📄 **[Pre-Requisite](https://github.com/prafulpatel16/mgn-aws-project01/blob/master/migration/A-Phase%201-AWS%20Application%20Discovery%20%26%20TCO%20Analysis/0.Pre-requisite.md)**
   - 📄 **[Discovery Service Deployment](https://github.com/prafulpatel16/mgn-aws-project01/blob/master/migration/A-Phase%201-AWS%20Application%20Discovery%20%26%20TCO%20Analysis/1.Deploy.md)**
   - 📄 **[High-Level TCO Analysis](https://github.com/prafulpatel16/mgn-aws-project01/blob/master/migration/A-Phase%201-AWS%20Application%20Discovery%20%26%20TCO%20Analysis/2.HighLevel-TCO-Analysis.md)** 
   - 📄 **[Complete AWS Migration Documentation](https://github.com/prafulpatel16/mgn-aws-project01/tree/master/docs)** 

  
## 🏗️ Project Architecture

### 🔹 **On-Premises Setup**
- **Web Application**: Runs on a local server using **Apache** or **NGINX**.
- **Database Server**: MySQL database deployed locally, connected to the web application.

![alt text](migration/images/web01.png)

## 🛠️ Key Technologies Used

### **On-Premises Environment**
- **Web Server**: Apache/NGINX.
- **Database**: MySQL.

### **AWS Environment**
- **AWS ADS**: Captures existing VMs data from on-premises VMs to AWS Migration Hub.
    - Collects Data: Technical Information , Performance Information, Network information
- **AWS DMS**: Migrates data from on-premises MySQL to AWS RDS MySQL.
- **AWS RDS**: Managed MySQL database service.
- **AWS Client VPN**: Provides secure connectivity between on-premises and AWS.
- **AWS VPC**: Virtual Private Cloud with subnets for isolating resources.
- **AWS EC2**: Virtual servers to host the web application (optional).
- **AWS IAM**: Role-based access control for secure migration.

---
## 🎯 Key Components

### 🗄️ **AWS ADS**
- Ensures a seamless information and Data collecting from on-premises VMs to **AWS Migration Hub**,**Data Collector**, **Servers**.

### 🗄️ **AWS DMS**
- Ensures a seamless database migration from on-premises MySQL to AWS RDS with options for **full-load** and **CDC (Change Data Capture)**.

### 🔐 **AWS VPN**
- Provides secure connectivity to AWS resources from your on-premises environment.

### 📦 **AWS RDS**
- Offers a managed database service with **automatic backups**, **scalability**, and **high availability**.

### 🏗️ **AWS VPC and Networking**
- Includes **private** and **public subnets**, **NAT Gateway**, **Internet Gateway**, and **Route Tables** for secure network configuration.

---

### 🔹 **AWS Setup**
1. **Networking**:
   - AWS VPC with **public** and **private subnets**.
   - AWS Client VPN for secure connectivity between on-premises and AWS.

2. **Database**:
   - RDS MySQL instance for **managed database services**.
   - Data migration using AWS Database Migration Service (**DMS**).

3. **Web Application**:
   - Deployed on **AWS EC2** in a **private subnet**.
   - Served using a **load balancer** (optional for scaling).

---

## 📊 High-Level Workflow

### **1️⃣ Pre-Migration**
- 🔍 **Assess Current Architecture**: Analyze the on-premises architecture and workloads, identifying dependencies and compatibility for migration.
- 🛠️ **Install and Configure AWS ADS Agents**: Deploy AWS Discvoery Agents (ADS) agents on source systems to capture data for migration.
- 🛠️ **Install and Configure AWS DMS Agents**: Deploy AWS Database Migration Service (DMS) agents on source systems to capture data for migration.
- 🏗️ **Set Up AWS Infrastructure**:
  - Create and configure **VPC** with public and private subnets.
  - Set up **RDS** for the target database.
  - Configure **VPN** for secure connectivity between on-premises and AWS.

---

### **2️⃣ Migration Execution**
- 🚀 **Migrate Data Using AWS DMS**:
  - Perform a **full-load migration** to transfer all existing data.
  - Enable **CDC (Change Data Capture)** to migrate real-time changes.
- 🔐 **Configure Secure Connectivity**:
  - Use **AWS Client VPN** to establish secure communication between the on-premises database and AWS.
- 📈 **Monitor Migration Progress**:
  - Use **AWS DMS logs** and **CloudWatch metrics** to track the migration process and troubleshoot any issues.

---

### **3️⃣ Post-Migration**
- ✅ **Validate Data Integrity**:
  - Compare source and target databases to ensure schema and data consistency.
- ⚙️ **Optimize Performance**:
  - Adjust RDS instance type and configurations for better performance and cost efficiency.
  - Implement indexing and query optimization where necessary.
- 📊 **Monitor and Scale**:
  - Use **AWS CloudWatch** to monitor database performance.
  - Scale the application and database resources as needed to meet workload requirements.

---

### 🧪 **Testing and Validation**
- 🛠️ **Run Validation SQL Scripts**:
  - Use SQL queries to verify data consistency, such as row counts and checksum comparisons between the source and target databases.
- 🔗 **Verify Application Functionality**:
  - Test the web application to ensure it connects successfully to the migrated RDS instance and operates as expected.
- 📝 **Analyze Logs**:
  - Review **DMS migration logs** and CloudWatch metrics for any errors, discrepancies, or missed data during migration.

---

### 🚀 **AWS Cloud Migration - Phase 1: Application Discovery & TCO Analysis**  

Cloud migration is no longer a question of *if* but *when and how*. Organizations are rapidly moving from **on-premises** to **AWS Cloud** to enhance **scalability, security, and cost efficiency**. But **how do you ensure a seamless migration?**  

👉 **Phase 1 starts with AWS Application Discovery Service (ADS)**, helping you assess **current infrastructure, dependencies, and costs** before making the move.  

🔹 **Why Migrate?**  
✅ Reduce **operational costs** (TCO)  
✅ Enhance **scalability & performance**  
✅ Strengthen **security & compliance**  
✅ Enable **automation & innovation**  

🔹 **How to Migrate?**  
1️⃣ **Discovery & Assessment** 📊  
   - Use **AWS Migration Hub & ADS** to analyze workloads.  
   - Deploy **Discovery Agents** to gather system metrics.  
   - Conduct **Migration Readiness Assessment (MRA)** to evaluate business & tech alignment.  

2️⃣ **Planning with TCO & RACI** 🛠️  
   - Perform **High-Level TCO Analysis** for cost estimation.  
   - Define **roles & responsibilities** using **RACI Matrix**.  
   - Optimize resources for **right-sized AWS migration**.  

3️⃣ **Migration Execution** 🔄  
   - Migrate databases using **AWS DMS**.  
   - Use **AWS Client VPN & Direct Connect** for secure connectivity.  
   - Implement **CloudWatch & Security Best Practices**.  

📍 **Follow Detailed Documentation on GitHub**:  
🔗 **📌 Discovery Service Deployment:**  [GitHub Link](https://github.com/prafulpatel16/mgn-aws-project01/blob/master/migration/A-Phase%201-AWS%20Application%20Discovery%20%26%20TCO%20Analysis/1.Deploy.md)  

🔗 **📌 High-Level TCO Analysis:**  [GitHub Link](https://github.com/prafulpatel16/mgn-aws-project01/blob/master/migration/A-Phase%201-AWS%20Application%20Discovery%20%26%20TCO%20Analysis/2.HighLevel-TCO-Analysis.md)

🔗 **📌 Complete AWS Migration Docs:**  [GitHub Link](https://github.com/prafulpatel16/mgn-aws-project01/tree/master/docs)  

💡 **Stay Updated with Tech Content:** [📌 Praful’s Blog](https://www.praful.cloud)  

🚀 **Migrate Smart, Optimize Costs, and Build Scalable Cloud Solutions!** 💡 #AWS #CloudMigration #ApplicationDiscovery #TCO #DevOps #AWSMigration #InfrastructureOptimization


## 📖 References

- [AWS Database Migration Service (DMS)](https://aws.amazon.com/dms/)
- [AWS RDS](https://aws.amazon.com/rds/)
- [AWS Client VPN](https://aws.amazon.com/vpn/client-vpn/)

---

## 🤝 Contributing

Contributions are welcome! Please check the [CONTRIBUTING.md](CONTRIBUTING.md) file for guidelines on how to contribute to this project.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🧑‍💻 Author

Created and maintained by **Praful Patel**.  
For inquiries, visit [Praful's GitHub](https://github.com/prafulpatel16).
For Tech, visit [Praful's Blog](https://www.praful.cloud).

---

