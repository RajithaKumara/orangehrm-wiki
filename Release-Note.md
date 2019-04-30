## OrangeRHM Version 4.3.1
**Release Date: ** <br>
**Release URL: **

### New Features
* Reset forgotten password
* Compatibility with PHP 7.2.17
* Compatibility with MySQL 5.7.26
* Compatibility with MariaDB 10.3.14

### Bug Fixes
* Pending leave request is not showing in the dashboard for admin or supervisor. <b> git Issue #470 </b> 
* Google OpenID Support. <b> git Issue #472 & #222 </b>
* French Add User not working <b> git Issue #452 </b>


## OrangeRHM Version 4.3
**Release Date: 2019-03-02** <br>
**Release URL: https://sourceforge.net/projects/orangehrm/files/stable/4.3/**

### New Features
* Market Place
   * Install or uninstall free add-on by admin users
   * Request paid add-on by admin users
   * View all compatible add-ons by all users
### Bug Fixes
   * French Add User not working <b> git Issue #452 </b>

## OrangeRHM Version 4.2.0.1
**Release Date: 2018-11-05** <br>
**Release URL: https://sourceforge.net/projects/orangehrm/files/stable/4.2.0.1**
### Bug Fixes
* Remove HTTPS restriction introduced in OrangeHRM 4.2 release
### New Features
* Add SimpleXML modules to pre-requisites check

## OrangeRHM Version 4.2
**Release Date: 2018-10-31** <br>
**Release URL: https://sourceforge.net/projects/orangehrm/files/stable/4.2**
### New Features
* Maintenance module - GDPR Compliance
   * Purge employee records
   * Purge candidate records
   * Access employee records
* Security Enhancements
   * Update .htaccess restrictions
   * Improve CSRF token validation
   * Resolve Path-Based vulnerability
   * Enable secure cookie attribute to application cookie
* Enhancement on OS installation error messages
### Bug Fixes
* Verify installation supports in different mysql ports
* Verify if pdo/mysqli has been enabled during installation
### Removed Features
* Remove unix_socket support at the installation
## OrangeRHM Version 4.1.2.1
**Release Date: 2018-09-07** <br>
**_Release URL:   https://sourceforge.net/projects/orangehrm/files/stable/4.1.2.1**
### Bug Fixes
* Installation fails if cURL is not enabled 
* Resolved issue with relative paths running into an error in Windows & Apache
* Resolved issue with supported environment version verification during installation

## OrangeRHM Version 4.1.2
**Release Date: 2018-08-31** <br>
**Release URL: https://sourceforge.net/projects/orangehrm/files/stable/4.1.2**
### Features
* Enhancement of System configuration wizard during Installation. Setup instance with user entered data during installation.
* Supported Language packs 
   * English
   * French
   * German
   * Spanish (Costa Rica)
   * Spanish
   * Dutch
   * Chinese (Traditional Han)
   * Chinese (Simplified Han)
* Support of CLI Installer

### Bug Fixes
* "Csrf token validation failed" message appears in Login screen even after trying to login with valid credentials <b> git Issue #247 </b>
* Incorrect version number in config file <b> git Issue #262 </b>
* cannot install in MySQL 5.7.23, supporting version is equal or lesser version than 5.7.22
* web Installer: "help" link should be changed with a new guide
* When change password by accessing Change Password link, system getting inaccessible

## OrangeHRM Version 4.1.1
_**Release Date: 2018-07-02**_ <br>
**_Release URL: [OrangeHRM 4.1.1](https://sourceforge.net/projects/orangehrm/files/stable/4.1.1**
### Features
* Verification of supported environment during the installation.
   * Supported PHP Version Range
       * Minimum version: 5.6
       * Maximum Version: 7.25
   * Supported MySQL Version Range
       * Minimum version: 5.5
       * Maximum Version: 5.7.22
   * Supported MariaDB Version Range
       * Minimum version: 5.5
       * Maximum Version: 10.3.7
* Usability Improvement when Adding User. Shows a message on adding a user when there are no employees added to the system.

###  Bug Fixes
* Recruitment - Vacancy page is crashed when a hiring manager is deleted in the system.
* Blank page when refreshing the login page after entering the invalid credentials.
* Leave is assigned as half day when specific time option is chosen for "End Day - Partial Day" option
* Leave - Internal Error is occurring when admin enters lengthy integer when adding an entitlement.
* PIM-Membership: does not add multiple records for a selected membership type to an employee
* Recruitment - Sorted by candidate list screen is leading to crash page when vacancy list is open in another tab.
* Google OpenId Provider not working in 4.1 <b> git Issue #222 </b>
* Can not install using web installer if the database is on MariaDB 10.2
* Unable to install the build for PHP 7.2 with any MySQL version.


## OrangeHRM Version 4.1
_**Release Date: 2018-04-26**_ <br>
_**Release URL: [OrangeHRM 4.1](https://sourceforge.net/projects/orangehrm/files/stable/4.1)**_
###  Features
* Integration with Toggl. Users can sync the time entries tracked in Toggl to OrangeHRM Time module.
* Enforcement of having a strong password for the user account.
* Compatability with LDAP Add-on
* Environment Compatability with PHP 7.1 & MariaDB 10.2
### Bug Fixes
* Security bug fixes.