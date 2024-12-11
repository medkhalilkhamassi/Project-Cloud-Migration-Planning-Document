
# Roadmap for Simulating TechCorp's On-Premises Infrastructure in Cisco Packet Tracer

This document outlines the step-by-step process to simulate TechCorp's on-premises infrastructure within Cisco Packet Tracer. The goal is to fully represent the network, servers, and services in a virtual environment.

---

## **1. Prepare the Network Topology**

- [ ] Add a **Layer 3 switch** to the workspace.
- [ ] Create VLANs for each department:
  - [ ] VLAN 10: IT
  - [ ] VLAN 20: Sales/CRM
  - [ ] VLAN 30: Developers
  - [ ] VLAN 40: Admin and Support
  - [ ] VLAN 100: Servers
- [ ] Assign IP addresses to VLAN interfaces for inter-VLAN routing.

---

## **2. Configure Core Network**

- [ ] Add additional **Layer 2 switches** if required for workstation connections.
- [ ] Connect all devices (workstations and servers) to the switches.
- [ ] Assign ports to appropriate VLANs.

---

## **3. Set Up Servers**

### **Active Directory and DNS Server**

- [ ] Add a server node for Active Directory and DNS.
- [ ] Assign to VLAN 10.
- [ ] Configure DNS with the domain `techcorp.local`.
- [ ] Create sample DNS entries for internal services (e.g., `crm.techcorp.local` -> `192.168.20.2`).

### **CRM Application Server**

- [ ] Add a server node for the CRM application.
- [ ] Assign to VLAN 20.
- [ ] Enable HTTP/HTTPS services.
- [ ] Create a simple HTML page simulating the CRM portal.

### **File Server**

- [ ] Add a server node for file sharing.
- [ ] Assign to VLAN 100.
- [ ] Enable SMB services for file sharing.
- [ ] Configure departmental shares (e.g., `IT_Share`, `Sales_Share`).

### **Email Server**

- [ ] Add a server node for email services.
- [ ] Assign to VLAN 100.
- [ ] Enable SMTP and POP3/IMAP services.

### **GitLab Server**

- [ ] Add a server node for development tools.
- [ ] Assign to VLAN 30.
- [ ] Enable HTTP/HTTPS to simulate GitLab or a similar platform.

---

## **4. Add Workstations**

- [ ] Add PCs for each department:
  - [ ] IT (VLAN 10)
  - [ ] Sales/CRM (VLAN 20)
  - [ ] Developers (VLAN 30)
  - [ ] Admin and Support (VLAN 40)
- [ ] Configure PCs with static IPs or DHCP (optional).

---

## **5. Implement Internet Connectivity**

### **Edge Router**

- [ ] Add a router to simulate WAN connectivity.
- [ ] Connect the router to an ISP cloud node.
- [ ] Configure the router's WAN interface with a public IP (e.g., `203.0.113.1`).
- [ ] Enable NAT for internal devices to access the internet.

---

## **6. Simulate Security with a Firewall**

- [ ] Use a router to simulate firewall functionality.
- [ ] Add ACLs to control traffic:
  - [ ] Block unauthorized access between VLANs.
  - [ ] Restrict access to sensitive servers (e.g., file server).
- [ ] Test security rules by attempting restricted traffic flows.

---

## **7. Set Up Services**

- [ ] Configure **DNS** on the AD server.
- [ ] Set up **DHCP** (optional) on the Layer 3 switch or a server.
- [ ] Enable **file sharing** on the file server.
- [ ] Configure **email services** and test email exchange between workstations.

---

## **8. Validate the Setup**

- [ ] Test inter-VLAN routing by pinging devices in different VLANs.
- [ ] Access the CRM application from a workstation's browser.
- [ ] Mount shared folders from the file server on workstations.
- [ ] Send emails between devices using configured email clients.

---

## **9. Add Annotations and Documentation**

- [ ] Label all devices with their names, IP addresses, and VLANs in Packet Tracer.
- [ ] Save the Packet Tracer file as `TechCorp_OnPrem.pkt`.
- [ ] Document configurations (e.g., VLAN IDs, IP assignments) in a separate text or markdown file.

---

## **10. Backup and Refine**

- [ ] Save progress at each major step.
- [ ] Test for any connectivity or service issues and troubleshoot.
- [ ] Optimize the layout and clean up the topology for presentation.

---

## **Timeline (Optional)**

| Step                        | Estimated Time |
| --------------------------- | -------------- |
| Network Topology Setup      | 1 hour         |
| Server Configurations       | 2-3 hours      |
| Workstation Configurations  | 1 hour         |
| Internet and Security Setup | 1-2 hours      |
| Service Testing             | 1 hour         |
| Documentation and Backup    | 1 hour         |

---

This roadmap provides a clear path to simulate TechCorp's on-premises infrastructure in Cisco Packet Tracer. Follow each step carefully and validate your setup along the way.
