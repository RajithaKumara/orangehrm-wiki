[download](https://drive.google.com/drive/folders/1rsoUiPgIrz_q3xE9HRtE45z_je9O5iw7?ogsrc=32)

# Introduction

## Overview

OrangeHRM Open Source is a free and open source HR software that offers a wealth of feature rich modules to suit the needs of your business needs.

There are several ways to implement OrangeHRM Open source in your user environment.The most recommended method to implement the system is by using the default in-built Web Installer.
Purpose of this document

This installation guide describes step by step installation and configuration process of OrangeHRM using the in built Web-Installer. It is intended for experienced administrators and novices alike. However technical users who wish to manually configure OrangeHRM can refer the OrangeHRM FAQ.


Before you start
To install OrangeHRM, ensure that meet the Prerequisites.

### Prerequisites

The prerequisites are;

Apache HTTP Server 2.4.6 or later
MySQL 5.5 or later / MariaDB 5.5 or later,
PHP 7.0 or later

If you already have Apache HTTP web server (and PHP loaded as an Apache Module) and MySQL running, then you have everything you need. (Note: OrangeHRM requires PHP 7.0)

In case you don't have the requisites setup, you have two options.

1. Use OrangeHRM Appliance for Windows. Just install and use.

2. Use an AMP stack which has Apache, MySQL and PHP pre-configured to work together. See AMP stack for Windows if you are using Windows or else if you are using Linux, AMP stack for Linux.

If you want you could configure Apache, MySQL and PHP on you own manually. You can refer the OrangeHRM FAQ on how to install/configure them.

### AMP Stack for Windows

Recommended AMP stack for Windows is XAMPP for Windows. 

It is important that you make sure you download the Installer from the Basic Package and not the upgrades or developer packs as they may deviate from the prerequisites required . 

After downloading, start installing XAMPP for Windows.


You can choose the default installation location and click [Next]
When asked to "Install XAMPP Servers (Apache, MySQL, .....) as service?", select Yes
When asked "Install Apache 2 as service?", select Yes
When asked "Install MySQL as service?", select Yes

You may skip the other services by selecting no since they are not required for OrangeHRM


When you’re finish with installing XAMPP,select Yes to start the XAMPP control panel .

Note:

Remember to enable InnoDB support. See How to enable InnoDB support in MySQL.
If you use any firewall software (ie; Windows Firewall) if prompted please make sure that XAMPP services (Apache Web Server, MySQL) are exempted from the blocked list.
If you use Skype, this may result in a port conflict with Apache web-server included in XAMPP. Therefore make sure you restart Windows to make sure that XAMPP services start before Skype (then Skype will go for another free port).

### AMP Stack for Linux
 
Recommended AMP stack for Linux is XAMPP for Linux 1.7.7
 
Make sure you download complete stack(usually the biggest download out of the lot) and not the upgrades, developer packs, etc.
 
After downloading, install XAMPP Linux. Follow the instructions that comes with XAMPP Linux or given in the XAMPP site. For XAMPP users, Linux stack needs to be started 

manually. Refer to the stack documentation.


Note:

You will have to change the ownership of OrangeHRM files to nobody.nobody


Type the following in the shell. <orangehrm> is the path where the OrangeHRM files are located. 

Ex. /opt/xampp/htdocs/orangehrm-[version_no]/

$ chown -R nobody.nobody <orangehrm>


## Installation

This section will cover step by step installation process of OrangeHRM using the Web installer.

### Copying Files

Copy and extract OrangeHRM-[version_no].zip into the document root of the Apache HTTP Server. 

If you use XAMPP for Windows, default document root is located as follows:

    <XAMPP Installed Location>\htdocs\
            Eg:  C:\Program Files\xampp\htdocs

If you use XAMPP for Linux, default document root is located as follows:

    <XAMPP Installed Location>/htdocs/

After you copied the files in relevant location, initiate XAMPP server. Using a javascript enabled browser, type following location to as the URL to access the  Web Installer.

http://<webhost>/orangehrm-[version_no]/

Here, use localhost as <webhost> if it is installed in the machine you are currently working on (Eg: http://localhost/orangehrm-4.1.2.1/). 

Use IP address if it is remotely hosted (i.e. external to the machine you are using.) (Eg. http://122.1.1.18/orangehrm-4.1.2.1/ )

### Welcome Screen


Welcome screen states the version of OrangeHRM that will be installed. 

If you already have a running system of OrangeHRM implemented at your environment, It is recommend that you choose Upgrading instead of going in with installation process.

To process with the installation, click [Next]



### License Acceptance

Copy of the GNU GENERAL PUBLIC LICENSE will be provided to you at this screen.
 

 
To continue with the installation process, you will require to accept the terms and conditions mentioned in Licence. If you wish to do so, click [I Accept] button which will take you to the page of the installation process.

If you decline simply discontinue the installation and delete all OrangeHRM files you posses.
 
### Database Configuration

You will require to configure your database information here. It is recommended that you keep the default values which are already populated in the fields. 

Enter the relevant information about your MySQL database server and database users.
Click [Next] in Database Creation screen to continue.



Note: Privileged Database Users and OrangeHRM Database Users

Database Server users could be assigned different rights. For the web installer to create the OrangeHRM Database, you need to give a Database user account details (user-name/password) with permissions CREATE, ALTER, DROP, INSERT under the field Privileged Database User/Password.

Since OrangeHRM requires only permissions INSERT, UPDATE, SELECT and DELETE to interact with database, the web installer could create a separate database user account to for OrangeHRM. It is always recommended that you create a separate user account for OrangeHRM. To do so fill in OrangeHRM User details(user-name/password) as required and the web-installer would create the account for you.

Since the database user account details used by OrangeHRM are stored in plain text, it would be a security threat to have OrangeHRM use Privileged user account.

### System Check
In this step, the web installer will check whether the prerequisites are available in your environment. 

If you meet all the requirements, the responses will indicate in Green meaning that you have installed the correct versions of prerequisites in your environment and configured them to work in harmony.

Click [Next] button to proceed to the next step.

If your environment do not meet any of the prerequisites, system check response will indicate in red and the installation wizard will not allow you to proceed further. 

Status responses that indicate in gray letters also denotes that your system does not meet the optimum recommended requirements. However you will be able to continue with the installation as the existing requirements will be sufficient to run the system.

### System Configuration

Enter your organization details and Admin user details in this screen in order to create your instance. 

You will be logged into the system using the credentials you create in this step. Make sure you set a Admin username and password here where you can recall back in that stage.

### Confirmation
Summary of all the information collected to create your OrangeHRM instance will be shown in this screen. You can check whether information you entered are correct before the installation. Click [Install] to confirm the details and proceed with the installation.

### Installing

This screen will  show you the installation progress. Installation will take approximately 5-10 minutes depending on the performance of your system.
Once all components of the system are installed, Click [next] to continue.


If an error occurs during the installation process,the whole installation will be aborted. You will need to correct the relevant errors by going back to previous screen and start the installation again. Click [Clean Up Install] to go to previous pages to correct the error.

### Logging in to OrangeHRM

Use your user credentials that you created during system configuration to access the system as an Admin user. They will be populated by default in username and password fields once the installation is completed.  


 




