**What this chapter is about?**  

This chapter is about **Amazon EC2 (Elastic Compute Cloud)** and explains **how compute works in AWS**.  
It sets the foundation for **running servers, webstes, and applications in the cloud**.  

--- 

**What is Amazon EC2?**  
- EC2 = Elastic Compute Cloud  
- It provides Infrastructue as a Service (IaaS)
- Lets you rent virtual servers (VMs) on demand

📌 **Core idea of cloud computing**:  
Rent compute power when you need it, stop when you don’t.

---

**EC2 is More than Just a VM**  

At a high level, EC2 includes:  
- **EC2 Instances** -> Virtual machines
- **EBS Volumes** -> Virtual Storage (network-attached disks)
- **Elastic Load Balancer (ELB)** -> Distributes traffic
- **Auto-Scaling Group (ASG)** -> Automatically scales instances

📌 **Tip**: EC2 is an **ecosystem**, not a single feature.

---

**What can you choose when launching an EC2 instance?**  

**1. Operating System**
- Linux (most popular)
- Windows
- macOs

---

**2. Compute Power (CPU)**
- Number of vCPUs / cores
- Determines processing capability

---

**3. Memory (RAM)**
- More RAM = Better performance for memory-heavy apps

---

**4. Storage Options**
- **EBS** -> Network-attached storage file system (most common)
- **EFS** -> Shared network file system
- **Instance Store** -> Hardware-attached, very fast, but temporary

---

**5. Networking**
- Type of network interface
- Public IP assignment
- Network performance

---

**6. Security Group**
- Acts as a **Firewall**
- Controls **inbound and outbound traffic**

---

**7. EC2 User Data (Bootstrap Script)**
- A script that runs only once at first launch
- Used for **bootstraping** the instance

---

**EC2 User Data Explained (Very Important)**
**What is Bootstrapping?**
- Running commands automatically at instance startup

**Common Use Cases**:
- Install OS updates
- Install software (Apache, Nginx, Docker, etc.)
- Download files
- Configure applications

**📌 Key rules**:
- Runs only once
- Runs at first boot
- Executes as root user (sudo access)
- More commands = slower startup

---

**What This Chapter Teaches You**

- What EC2 is and why it’s central to AWS
- EC2 is on-demand, customizable compute
- You control:
  - OS
  - CPU
  - RAM
  - Storage
  - Network
  - Security
  - Startup automation
  - How AWS enables fast server provisioning
 
---

**Keywords to Remember**

- EC2
- Elastic Compute Cloud
- Infrastructure as a Service (IaaS)
- EC2 Instance
- Security Group
- User Data
- Bootstrapping

---

**Simple Exam Logic**

- **Need a server?** → EC2
- **Run commands at launch?** → User Data
- **Firewall for EC2?** → Security Group
- **Temporary high-speed storage?** → Instance Store
