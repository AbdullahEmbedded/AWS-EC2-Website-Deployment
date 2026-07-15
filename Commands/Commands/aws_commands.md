# AWS EC2 Deployment Commands

This document contains the Linux commands used to deploy a static website on an Amazon EC2 instance running Amazon Linux.

--- 

# 1. Connect to the EC2 Instance

```bash
ssh -i your-key.pem ec2-user@YOUR_PUBLIC_IP
```

**Purpose**

Connects securely to the EC2 instance using SSH.

---

# 2. Update System Packages

```bash
sudo yum update -y
```

**Purpose**

Updates all installed packages to the latest available versions.

---

# 3. Install Apache HTTP Server

```bash
sudo yum install httpd -y
```

**Purpose**

Installs the Apache web server.

---

# 4. Start Apache

```bash
sudo systemctl start httpd
```

**Purpose**

Starts the Apache service.

---

# 5. Enable Apache at Boot

```bash
sudo systemctl enable httpd
```

**Purpose**

Automatically starts Apache whenever the EC2 instance boots.

---

# 6. Check Apache Status

```bash
sudo systemctl status httpd
```

**Purpose**

Displays the current status of the Apache service.

---

# 7. Copy Website Files

Example:

```bash
sudo cp -r * /var/www/html/
```

**Purpose**

Copies the website files into Apache's default web directory.

---

# 8. Set File Permissions

```bash
sudo chmod -R 755 /var/www/html
```

**Purpose**

Grants the correct permissions to website files.

---

# 9. Restart Apache

```bash
sudo systemctl restart httpd
```

**Purpose**

Restarts Apache after making changes.

---

# 10. Verify Website

Open your browser and visit:

```
http://YOUR_PUBLIC_IP
```

If everything is configured correctly, your website should load successfully.

---

# Skills Demonstrated

- Linux Commands
- SSH
- Amazon EC2
- Apache HTTP Server
- Website Deployment
- AWS Cloud Computing
