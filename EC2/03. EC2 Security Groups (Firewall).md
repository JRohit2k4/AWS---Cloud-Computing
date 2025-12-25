**EC2 Security Groups (Firewalls)**  

This chapter explains **Security Groups**, which acts as a **virtual firewall** for EC2 instnces in AWS. They control **who can access your EC2 instances and on which ports**, both for inbound (incoming) and outbound (outgoing) traffic.  

Security frouos are **simple but critical** for AWS network security.They are **allow-only firewalls**, meaning you explicitly define what traffic is allowed; everything else is blocked by default.  

They work **outside the EC2 instance**, so if traffic is blocked, the instance never even sees it.

---

**Key Concepts Explained**

**1. What Security Groups Do**
- Control **inbound traffic** (internet -> EC2)
- Control **outbound traffic** (EC2 -> internet)
- Act as a **firewall** at the **instance level**
- Rules are based on:
   - Port
   - Ptotocol (TCP)
   - Source (IP address or another security group)

---

**2. Important Security Group Rules**
- **Inbound traffic**: Blocked by default
- **Outbound traffic**: Allowed by default
- Only **ALLOW rules** exist (no deny rules)

Example:
- Allow SSH (port 22) from your **IP**
- Allow HTTP (port 80) from **0.0.0.0/0** (everyone)

---

**3. IP Address Rules**
- `0.0.0.0/0` -> Allows traffic from everywhere
- Specific IP -> Restric access to **one location**
- Support both **IPv4 and IPv6**

---

**4. Security Groups & EC2 Relationship**
- One **security group** -> **multiple EC2 instances**
- One **EC2 instance** -> **Multiple security groups**
- Security groups are tied to:
   - Region
   - VPC
- You **must recreate** them if you change region or VPC

---

**5. Timeout vs Connection Refused**
- **Timeout** -> Security group issue (traffic blocked)
- **Connection refused** -> App/service not running, SG is fine

This distinction is **very important for exams**.

---

**6. Best Practice (Real-World Top)**
- Keep **SSH in a separate security group**
- SSH is sensitive and easier to manage independently

---

**7. Security Group Refrencing (Advanced but Important)**
- Security groups can **reference other security groups**
- This allows EC2 instances to communicate **without using IPs**
- Very useful for:
   - Load balancers
   - Microservices
   - Auto Scaling
Example:
- SG-A allows inbound traffic from SG-B
- Any instance with SG-B can access instances with SG-A

---

**Must-Know Ports for the Exam**

| Port | Protocol | Use                   |
| ---- | -------- | --------------------- |
| 22   | SSH      | Linux EC2 login       |
| 21   | FTP      | File transfer         |
| 22   | SFTP     | Secure file transfer  |
| 80   | HTTP     | Unsecured web traffic |
| 443  | HTTPS    | Secured web traffic   |
| 3389 | RDP      | Windows EC2 login     |

---

**What This Chapter Teaches You**

By the end of this chapter, you should understand:

- How AWS secures EC2 instances
- How traffic is allowed or blocked
- Why security groups are **stateless allow-only firewalls**
- How to diagnose **connection issues**
- How AWS avoids IP-based rules using SG referencing
- Which ports matter for the **AWS exam**

---
