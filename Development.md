# Development Guidelines 
## How to setup 
You can clone the project to your local computer as follows 
```
    git clone git@github.com:orangehrm/orangehrm.git
```
After that, you have to execute the following commands to update composer dependencies 
```
    composer install -d symfony/lib
    composer dump-autoload -o -d symfony/lib
```
The orangehrm project develops with symfony framework and followings commands help to build the doctrine model and publish local assets. 
```
   php symfony orangehrm:publish-assets
   php symfony doctrine:build-model
   php symfony cc
``` 
## How to installl via command line
Update installer/config.ini file with your local values.
Execute the following command to install via cli.
```
./installer/cli_install.sh
```
## How to execute unit tests
Unit tests can be execute as follows
```
symfony/lib# vendor/bin/phpunit ../test/PluginAllTests.php
```

## How to change version number 
    php devTools/general/update-version.php [old version] [new version]