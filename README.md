# Keeper-of-the-Chronicles ( Blue Ajah 🌀 )

🚫 No-SSH EC2 Project: Understanding AWS Security Groups


---

### 🧰 What you need to have ready

---

- An active AWS account

- Basic familiarity with AWS Console

- A key pair (.pem) downloaded when launching the instance

- Terminal (for macOS/Linux)

---

### 📦 Part 1: Create an AWS EC2 Instance

---

- **Log in** to your AWS Management Console.

- Go to **EC2 → Instances** and click **Launch Instance**.

- Under *Name and tags*, name your instance any name of your choice (e.g., `Lawurusinstance-ssh`).

- Choose an Amazon Machine Image (AMI):
   - Recommended: **Amazon Linux 2023**

- Select an instance type:
   - **t2.micro** or **t3.micro** (Free Tier eligible)

- Under *Key pair (login)*, select an existing key pair or create a new one. **Download the `lawuruassign1.pem` file.**

- Scroll to *Network settings* → Click **Edit**.

- Proceed to **Part 2** before finalizing and launching the instance.

---

### 🔐 Part 2: Create & Configure a Security Group

---

- Under *Network settings → Firewall (security groups)*:
   - Click **Create security group**.

- Name it:  
   - **Security group name:** `No-SSH-Access`  
   - **Description:** `Block all SSH inbound connections`

- Remove any default **SSH (port 22)** inbound rule.

- Allow only necessary rules (e.g., HTTP or HTTPS) if needed.

- Click **Create security group**.

- Attach the new security group to your EC2 instance.

- Click **Launch instance**.

---

### 🚫 Part 3: Attempt SSH Access (Expect Failure)

---


### 🖥 macOS/Linux (Using Terminal)

```bash
chmod 400 lawuruassign1.pem
ssh -i lawuruassign1.pem ec2-user@34.234.76.114
```

Response:

```bash
ssh: connect to host 34.234.76.114 port 22: Operations time out
```

---

_The wheel of time reference is everything if you know Leane Sedai_ 💋💋

---
 
