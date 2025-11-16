

## **Objective**  
The objective of this task is to help you **install and configure Splunk on a Kali machine**. By completing this task, you will have Splunk up and running to collect and analyze security logs.

---

## **Lab Setup**  
### **Requirements**  
- **System:** Kali
- **Tools Required:**  
  - **Splunk Enterprise (Free version for local setup)**  
  - **Terminal (Command Line Access)**  

---

## **Steps to Install and Configure Splunk on Ubuntu**

### **Step 1: Download Splunk**
1. Open **Terminal** and download Splunk using `wget`:
   ```
   wget -O splunk-9.3.0-51ccf43db5bd-linux-2.6-amd64.deb    
   ```
  "https://download.splunk.com/products/splunk/releases/9.3.0/linux/splunk-9.3.0-51ccf43db5bd-linux-2.6-amd64.deb"

    
2. Once downloaded, install Splunk:
```
sudo dpkg -i sudo dpkg -i 'splunk-9.3.0-51ccf43db5bd-linux-2.6-amd64.deb'
```

### Step 2: Enable Splunk as a Service
1.  Create dirictory
``` 
mkidr -p /opt/splunk/bin 
```
2. Move to the Splunk installation directory:
```
cd /opt/splunk/bin
```
3. Accept the license agreement and enable Splunk at boot:
```
sudo ./splunk enable boot-start --accept-license
```
4. Start Splunk:
```
sudo ./splunk start
```
5. When prompted, set up an admin username and password.

### Step 3: Access Splunk Web Interface
1. Open a web browser and go to:
```
http://<your-server-ip>:8000
```
2. Log in with the admin credentials created earlier.
   

## Conclusion
 Successfully installed Splunk on an Ubuntu machine.  
 Configured Splunk as a service and enabled auto-start.  


## Submission
![image alt](https://github.com/noor-nas24/Spl_LAB_025/blob/ef80df6ccc91a36c2a5d5dd2d1f32b4c43deb7b8/splunk.png)
