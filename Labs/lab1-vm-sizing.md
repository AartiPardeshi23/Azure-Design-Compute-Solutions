# AZ-305 Module 08 - Lab 1: Virtual Machines – Sizing and Availability

## 🎯 Objective
Learn to create a Virtual Machine (VM) and understand sizing, regions, and availability options.

---

## 🧰 Prerequisites
- Azure Free or Paid Account
- Access to [https://portal.azure.com](https://portal.azure.com)

---

## 🪜 Steps

### Step 1: Create a Resource Group
1. Search **Resource Groups** → **+ Create**
2. Name: `rg-az305-vm`
3. Region: `East US`
4. Review + Create → Create

---

### Step 2: Create a Virtual Machine
1. Search **Virtual Machines** → **+ Create → Azure Virtual Machine**
2. Fill in:
   - Resource group: `rg-az305-vm`
   - Name: `vm-size-demo`
   - Region: East US
   - Availability options: *No infrastructure redundancy required*
   - Image: Ubuntu Server 22.04 LTS
   - Size: **Standard_B1s**
   - Username: `azureuser`
   - Password: `Azure@12345!`
   - Inbound ports: SSH (22)
3. Review + Create → Create

---

### Step 3: Check VM Size Information
- Go to your VM → **Overview → Size**
- Click **Change size** to view options and compare:
  - vCPUs
  - Memory (GB)
  - Disk Type
  - Hourly Cost

---

### Step 4: Try Different Availability Options
- Create another VM using **Availability Zone → Zone 1**
- Observe how it is placed in a separate data center within the region.

---

### 🧠 Key Concepts
| Concept | Explanation |
|----------|-------------|
| **B-Series** | Burstable VMs for dev/test |
| **D-Series** | General-purpose workloads |
| **E-Series** | Memory-optimized |
| **Availability Zones** | Physically separate datacenters in a region |

✅ You now understand VM sizing and availability configuration.
