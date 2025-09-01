# EC2 Windows Server Instance Creation

### Project Overview
This project outlines the steps for creating and managing an Amazon EC2 (`Elastic Compute Cloud`) instance on `Amazon Web Services` (`AWS`). The lab focuses on launching a `Windows Server 2016` instance, configuring a key pair for secure access, and preparing for remote server management via `RDP` (`Remote Desktop Protocol`).

### Goals
* Understand the process of creating an `EC2` instance.
* Learn to select the appropriate `AMI` (`Amazon Machine Image`) and instance type.
* Master the creation and management of key pairs for instance login.
* Prepare for remote connectivity to the `EC2` instance.

### Task Summary
* **Task 1: Navigate to EC2 Service and Initiate Instance Launch:** Logging into the `AWS Management Console`, navigating to the `EC2` service, and starting the new `EC2` instance creation process.
* **Task 2: Name the Instance and Select Operating System (AMI):** Naming the `EC2` instance "`first-ec2-instance`" and selecting the `Microsoft Windows Server 2016 Base AMI` as its operating system.
* **Task 3: Choose Instance Type and Create Key Pair for Login:** Choosing the instance type as `t2.micro`, and creating and downloading a new key pair named "`win2016_keypair_1`" in `.pem` format for secure login.
* **Task 4: Review and Launch Instance and Monitor Instance State:** Reviewing the instance summary, launching the `EC2` instance, and then monitoring its state until it transitions from "`Pending`" to "`Running`."
* **Task 5: Establish Remote Connection (RDP) and Retrieve Windows Password:** Establishing a remote connection via `RDP` by downloading the `RDP` file, obtaining the password, and using the private key to decrypt and retrieve the administrator password.
* **Task 6: Save Decrypted Password and Log In to the Instance via RDP:** Saving the decrypted administrator password as a text file and then executing the `RDP` file to log in to the `EC2` instance using the retrieved password.

### Step-by-Step Guide

---

### Task 1: Navigate to EC2 Service and Initiate Instance Launch

![Figure 1 - Log into the AWS Management Console](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure01_navigate_to_ec2.png)

1. Log into the `AWS Management Console`.
2. Navigate to "`Compute`," and select "`EC2`."
3. In the `EC2` dashboard, find "`Launch instance`" and start the new instance creation process.

![Figure 2 - Start the new EC2 instance creation process](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure02_start_ec2_creation.png)

### Task 2: Name the Instance and Select Operating System (AMI)

![Figure 3 - Name the instance](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure03_name_instance.png)

1. In "`Name and tags`," name the instance: "`first-ec2-instance`".
2. In "`Application and OS images`," choose "`Windows`" and select the "`Microsoft Windows Server 2016 Base AMI`".

![Figure 4 - Select the Microsoft Windows Server 2016 Base AMI](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure04_select_ami.png)

### Task 3: Choose Instance Type and Create Key Pair for Login

![Figure 5 - Select the t2.micro instance type](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure05_choose_instance_type.png)

1. Select the "`t2.micro`" instance type (`1 CPU`, `1 GB RAM`).
2. Under "`Key pair (login)`," create a new key pair named "`win2016_keypair_1`".
3. Ensure `.pem` format and download the key pair.

![Figure 6 - Download the key pair](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure06_download_keypair.png)

### Task 4: Review and Launch Instance and Monitor Instance State

![Figure 7 - Review the Instance Summary](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure07_review_and_launch.png)

1. Review the "`Instance Summary`" to verify configurations.
2. Keep default settings.
3. Click "`Launch instance`."
4. After launching, return to the `EC2` menu, navigate to "`Running instances`," find the new instance, and wait for its state to change from "`Pending`" to "`Running`".

![Figure 8 - Wait for its state to change from Pending to Running](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure08_monitor_instance_state.png)

### Task 5: Establish Remote Connection (RDP) and Retrieve Windows Password

![Figure 9 - Right-click and select Connect](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure09_establish_connection.png)

1. When the instance is "`Running`," right-click, and select "`Connect`."
2. Choose "`RDP client`" and download the `RDP` file.
3. Click "`Get Password`" (available after `4` minutes).
4. When "`Get Windows Password`" appears, load the `.pem` private key (from Task 3) to decrypt and retrieve the administrator password.

![Figure 10 - Decrypt and retrieve the administrator password](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure10_retrieve_password.png)

### Task 6: Save Decrypted Password and Log In to the Instance via RDP

![Figure 11 - Save the decrypted administrator password](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure11_save_password.png)

1. After decryption, save the `Windows 2016 AWS` host administrator password as a text file.
2. Execute the `RDP` file (from Task 5).
3. In the pop-up, enter the administrator password (from Task 5) and log in to the `EC2` instance.

![Figure 12 - Log in to the EC2 instance](https://github.com/iagsalazar1-cs/Cloud-Solutions/blob/main/01-EC2-Windows-Server-Instance-Creation/images/Figure12_login_ec2.png)
