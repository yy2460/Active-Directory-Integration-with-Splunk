# 🔒 **Active Directory Integration with Splunk** 🚀

Welcome to the **Active Directory Integration with Splunk** project! 🎉 This guide will take you through the steps of **setting up Active Directory (AD)** and integrating it with **Splunk** for powerful data analysis and monitoring. It also includes **troubleshooting tips**, **commands**, and **screen recordings** to make the process smoother.

---

## ✨ **Key Features of This Project** 🛠️

- 🌐 **Windows Server Setup**: Install and configure Windows Server as a Domain Controller.
- 🔍 **Splunk Universal Forwarder**: Setup and configure the Splunk forwarder for data forwarding.
- 💡 **Troubleshooting Tips**: Step-by-step guide to solving common issues like missing license terms or DNS misconfigurations.
- 🌎 **Domain Joining**: Seamlessly integrate Windows servers into a domain and resolve network issues.
- 📊 **Splunk Server Configuration**: Set up indexes, receiving ports, and verify data receipt.
- 💻 **Linux Integration**: Install and configure Kali Linux for penetration testing with Crowbar tool.

---

## 📜 **Setup Guide** 📚

Follow the steps below to configure Active Directory with Splunk:

### 1️⃣ **Install Windows Server** 🖥️
- During installation, **choose "Skip unintended installation"** to avoid the Microsoft license error.
  
### 2️⃣ **Configure Network & DNS** 🌐
- Make sure that **DNS points to your domain controller IP** (e.g., `192.168.10.7`).
- Ensure proper **network communication** by pinging your Splunk server.

```bash
ping 192.168.10.1
```

### 3️⃣ **Install Splunk Universal Forwarder** 🔄
- Download the Splunk Universal Forwarder and configure the **inputs.conf** file.

```ini
[monitor:///var/log/]
disabled = false
index = endpoint
```

### 4️⃣ Verify Communication ✅
Use the following command to check the status and ensure data forwarding is working fine.

```bash
net stop splunkforwarder
net start splunkforwarder
```
---

# 🚨 Troubleshooting Tips 🔧 
**❌ Error: Microsoft License Terms Missing** 

**Fix:** 

Make sure to select **"Skip unintended installation"** during the Windows Server setup.

**❌ Error: No Data Flowing to Splunk**

**Fix:**

- Ensure **network communication** is fine with ping test.
- Verify that **Splunk Forwarder is properly configured**.
- Restart the Splunk service using the following commands:
```bash
net stop splunkforwarder
net start splunkforwarder
```
**❌ Error: Unable to Join Domain**
**Fix:**

- Ensure **DNS is properly configured.**
- If using **VirtualBox**, consider setting a **static IP** instead of relying on DHCP.

---

## **📸 Screenshots & Visual Guides 📷**
 **🔑 Splunk Data Reception**

(Ensure the data is flowing from the forwarder to the Splunk dashboard.)

**🔌 Network Configuration Check**

(Verify DNS settings and network communication.)

---

## **💬 Commands and Configuration Files 📑**
**🖥️ Ping the Splunk Server**
```bash
ping 192.168.10.1
```
## **📝 Splunk Forwarder Configuration (inputs.conf)**
```ini
[monitor:///var/log/]
disabled = false
index = endpoint
```
## 🔄 Restart Splunk Forwarder Service
```bash
net stop splunkforwarder
net start splunkforwarder
```
---

## 🎥 Recordings and Demos 📹
**1️⃣ Domain Joining Process**
A step-by-step **video tutorial** on how to join a domain and troubleshoot common issues like DNS misconfigurations. Click here to watch the video.

**2️⃣ Splunk Forwarder Setup**
Watch the **screen recording** for configuring the Splunk forwarder and checking if data is properly received. Watch on YouTube.

**3️⃣ Linux Penetration Testing with Kali**
Learn how to use **Kali Linux** for penetration testing in your Active Directory environment using **Crowbar**. Watch here.

---

## 🛠️ Tools & Technologies Used 🖥️
- **Windows Server** (2016/2019)
- **Splunk** (Universal Forwarder & Enterprise)
- **Kali Linux** (for penetration testing)
- **VirtualBox** (for virtualization)
- **Crowbar** (for brute-forcing credentials)
- **Python** (for automation and testing)

---

## 🎯 Important Tips 💬
- Ensure the **correct Splunk index** is created to receive data.
- Always check the **Splunk listening port** (default: 9997).
- If using **VirtualBox**, make sure to configure **static IPs** when using multiple 
  virtual machines to avoid DHCP issues.

---
## 🔗 Useful Links 🌐
- Splunk Documentation
- Kali Linux Documentation
- Windows Server Setup Guide

---
