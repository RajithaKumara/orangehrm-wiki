
## Overview

This Guide describes how to install OrangeHRM. It is intended for experienced administrators and novices alike. After installation, you can configure users and do other administrative tasks. To install OrangeHRM, ensure that you have the appropriate Pre-requisites: See Pre-requisites

## Pre-requisites

The pre-requisites are;

    Apache HTTP Server 1.3 or later
    MySQL 5.1.6 or later
    PHP 5.3.0 or later

If you already have Apache HTTP web server (and PHP5 loaded as an Apache Module) and MySQL running, then you have everything you need. (Note: OrangeHRM requires PHP5)

In case you don't have the requisites setup, you have two options.
Use OrangeHRM Appliance for Windows. Just install and use.
Use an AMP stack which has Apache, MySQL and PHP pre-configured to work together. See AMP stack for Windows if you are using Windows or else if you are using Linux, AMP stack for Linux.

If you want you could configure Apache, MySQL and PHP on you own manually. You can refer the OrangeHRM FAQ on how to install/configure them.

AMP stack for Windows

Remember to enable InnoDB support. See How to enable InnoDB support in MySQL.

Recommended AMP stack for Windows is XAMPP Windows 1.7.7

Notice: make sure you download the Installer from the Basic Package and not the upgrades, developer packs, etc.

After downloading, start installing XAMPP for Windows.

You can choose the default installation location and click Next
When asked to "Install XAMPP Servers (Apache, MySQL, .....) as service?", select Yes
When asked "Install Apache 2 as service?", select Yes
When asked "Install MySQL as service?", select Yes
You may skip the other services by selecting no since they are not required for OrangeHRM
Select Yes to start the XAMPP control panel too.

Notice:

    If you use any firewall software (ie; Windows Firewall) if prompted please make sure that XAMPP services (Apache Web Server, MySQL) are exempted from the blocked list.
    If you use Skype, this may result in a port conflict with Apache web-server included in XAMPP. Therefore make sure you re-start Windows to make sure that XAMPP services start before Skype (then Skype will go for another free port).

AMP stack for Linux
Remember to enable InnoDB support. See How to enable InnoDB support in MySQL.

Recommended AMP stack for Linux is XAMPP Linux 1.7.7

Notice: make sure you download complete stack(usually the biggest download out of the lot) and not the upgrades, developer packs, etc.

After downloading, install XAMPP Linux. Follow the instructions that comes with XAMPP Linux or given in the XAMPP site.
Remember to start the stack.
Notes

You will have to change the ownership of OrangeHRM files to nobody.nobody
Type the following in the shell. <orangehrm> is the path where the OrangeHRM files are located.

    Ex. /opt/xampp/htdocs/orangehrm-[version_no]/

    $ chown -R nobody.nobody <orangehrm>

Please remember the location you installed XAMPP. It will be required later.
Installation
Copying files

Copy OrangeHRM-[version_no].zip into the document root of the Apache HTTP Server.
Notes

If you used XAMPP for Windows, document root is

    <XAMPP Installed Location>\htdocs\

    ex. C:\Program Files\xampp\htdocs

If you used XAMPP Linux AMP stack, document root is

    <XAMPP Installed Location>/htdocs/

Extracting

Extract OrangeHRM-[version_no].zip into the same folder, which would extract everything into a directory called 'orangehrm-[version_no]'.
Web Installation

Using a JavaScript enabled browser go to http://<webhost>/orangehrm-[version_no]/

Where <webhost> is localhost if it is installed in the machine you are currenty working on, IP address if it is remotely hosted (i.e. external to the machine you are using.)

See Web Installation.
Recommended Browsers

    Mozilla Firefox 12.
    Microsoft® Internet Explorer 9.
