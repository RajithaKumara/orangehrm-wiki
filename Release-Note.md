## OrangeRHM Version 4.1.2
**Release Date: 2018-08-31**
_**Release URL: **_
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
**Release Date: 2018-07-02**
**_Release URL: https://sourceforge.net/projects/orangehrm/files/stable/4.1.1/orangehrm-4.1.1.zip/download_**
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
_**Release Date: 2018-04-26**_
_**Release URL: https://sourceforge.net/projects/orangehrm/files/stable/4.1/orangehrm-4.1.zip/download**_
###  Features
* Integration with Toggl. Users can sync the time entries tracked in Toggl to OrangeHRM Time module.
* Enforcement of having a strong password for the user account.
* Compatability with LDAP Add-on
* Environment Compatability with PHP 7.1 & MariaDB 10.2
### Bug Fixes
* Security bug fixes.