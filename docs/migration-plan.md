
# Cloud Migration Planning: TechCorp Solutions

This document provides detailed information to kickstart the migration planning phase for TechCorp Solutions, simulating the process of transitioning their infrastructure from an on-premises setup to Microsoft Azure.

---

## **1. Current Infrastructure Overview**

### **On-Premises Servers**

- **Number of Servers**: 10
- **Operating Systems**:
  - 4 Linux servers (CentOS 7)
  - 6 Windows Servers (2016 and 2019)
- **Roles and Workloads**:
  - **Linux Servers**:
    - 2 for CRM application backend.
    - 1 for hosting internal wikis and documentation (MediaWiki).
    - 1 for hosting development tools (e.g., GitLab).
  - **Windows Servers**:
    - 2 for the SQL Server database for the CRM.
    - 1 for file storage (SMB shares).
    - 1 for hosting the Exchange email server.
    - 2 for Active Directory and authentication.

---

### **Network Infrastructure**

- **Firewalls**: Sophos hardware firewall.
- **Switches**: Layer 3 switches for VLAN segmentation.
- **Internet Connectivity**: 1 Gbps leased line.
- **VPN Access**: IPsec for remote workers.

---

### **Applications**

- **CRM**: Custom-built application with web and mobile interfaces.
- **Email**: Microsoft Exchange Server (on-premises).
- **Development Tools**: GitLab (self-hosted).
- **File Storage**: NAS for large file storage (connected to the Windows server).

---

### **Storage**

- **Total Capacity**: 50 TB (70% utilized).
- **Data Breakdown**:
  - CRM database: ~5 TB.
  - File shares: ~25 TB.
  - Email archives: ~10 TB.
  - Development tools and repositories: ~5 TB.

---

### **User Base**

- **Employees**: 200
- **Active Directory Accounts**: Managed on-premises.
- **User Roles**:
  - IT Team: 10 users.
  - Sales and CRM Users: 80 users.
  - Developers: 30 users.
  - Admin and Support Staff: 80 users.

---

## **2. Business Goals**

1. **Scalability**:
   - Handle peak usage during seasonal campaigns.
   - Easily add resources as the business grows.
2. **Cost Reduction**:
   - Minimize maintenance costs of aging hardware.
   - Pay-as-you-go model for infrastructure usage.
3. **Improved Security**:
   - Enhance compliance with ISO 27001 standards.
   - Centralized security management.
4. **Disaster Recovery**:
   - Reduce recovery time objective (RTO) and recovery point objective (RPO).
   - Implement a geographically redundant backup solution.

---

## **3. Migration Goals**

1. Migrate the CRM application and its database to Azure.
2. Move file storage to Azure Blob Storage or Azure File Shares.
3. Transition email services to Microsoft 365 (Exchange Online).
4. Set up development tools (e.g., GitLab) on Azure Virtual Machines or Azure DevOps.
5. Modernize Active Directory with Azure Active Directory integration.
6. Implement centralized monitoring and governance for all resources.

---

## **4. Challenges and Risks**

1. **Downtime**: Minimizing service disruptions during the migration.
2. **Data Migration**: Ensuring the integrity and security of sensitive data.
3. **Legacy Applications**:
   - Compatibility of the CRM application in a cloud environment.
   - Refactoring required to optimize for Azure.
4. **Training**: Upskilling the IT team on Azure management.

---

## **5. Azure Services for Migration**

### **Compute**

- Azure Virtual Machines for legacy applications.
- Azure App Service for the CRM web application.

### **Storage**

- Azure Blob Storage for unstructured data.
- Azure File Shares for SMB file shares.
- Azure SQL Database for the CRM database.

### **Identity**

- Azure Active Directory for identity and access management.
- Azure AD Connect for hybrid identity scenarios.

### **Networking**

- Azure VPN Gateway for secure remote access.
- Azure Firewall for centralized security management.

### **Backup and Disaster Recovery**

- Azure Backup for file-level backups.
- Azure Site Recovery for VM replication and failover.

---

## **6. Data to Gather During the Discovery Phase**

1. **Infrastructure Inventory**:
   - Hardware details (CPU, RAM, storage capacity).
   - Operating system versions and patch levels.
   - Application dependencies and configurations.

2. **Application Usage**:
   - Peak and average usage metrics.
   - API usage patterns and dependencies.
   - Data sensitivity and compliance requirements.

3. **Network Configuration**:
   - Firewall rules and NAT configurations.
   - VPN details for remote connectivity.
   - Current IP addressing and DNS setup.

4. **Storage Details**:
   - Data types and growth patterns.
   - Frequency of access (hot, cold, or archival data).
   - Backup and retention policies.

5. **User Roles and Access**:
   - Permissions and roles for current Active Directory users.
   - Access controls for shared resources.

---

## **7. Tools for Assessment**

1. **Azure Migrate**:
   - Assess server readiness for migration.
   - Dependency mapping for applications.
2. **Azure Pricing Calculator**:
   - Estimate Azure costs for compute, storage, and networking.
3. **Performance Monitoring Tools**:
   - Collect baseline performance metrics for applications and servers.
   - Tools like PRTG or SolarWinds for real-time monitoring.
4. **Network Assessment**:
   - Bandwidth requirements for data migration.
   - Tools like iperf to test network throughput.
