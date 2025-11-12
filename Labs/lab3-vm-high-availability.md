# AZ-305 Module 08 - Lab 3: Deploy Virtual Machines with High Availability

## 🎯 Objective
Deploy two VMs inside an Availability Set and load balance them for high availability.

---

## 🪜 Steps

### Step 1: Create a Resource Group
1. Name: `rg-az305-ha`
2. Region: East US

---

### Step 2: Create Availability Set
1. Search **Availability Sets** → **+ Create**
2. Resource group: `rg-az305-ha`
3. Name: `as-az305`
4. Fault domains: 2
5. Update domains: 5
6. Review + Create → Create

---

### Step 3: Create Two VMs in the Availability Set
#### VM 1:
- Name: `vm-az305-01`
- Availability set: `as-az305`
- Image: Ubuntu 22.04 LTS
- Size: Standard_B1s
- Username: `azureuser`
- Password: `Azure@12345!`
- Inbound ports: SSH (22)

#### VM 2:
- Name: `vm-az305-02`
- Same settings as above

---

### Step 4: Install Web Server
SSH into both VMs and run:
```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx

### Step 5: Create a Load Balancer

1.  Search **Load Balancers** → **\+ Create**
    
2.  Resource group: `rg-az305-ha`
    
3.  Name: `lb-az305`
    
4.  Type: **Public**
    
5.  SKU: **Standard**
    
6.  Frontend IP: Create new → `frontend`
    
7.  Backend pool: Add both VM NICs
    
8.  Health probe: TCP port 80
    
9.  Load balancing rule: Port 80 → backend pool
    

* * *

### Step 6: Test High Availability

*   Open the Load Balancer public IP in a browser.
    
*   Stop one VM → refresh → site still loads.
    

✅ You have a working HA setup using Availability Sets and Load Balancer.