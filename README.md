# Magento_Local_Setup
Setup Magento 2.3.7 in Local 





### SETUP FOR MAGENTO - 2.3.7 
--------------------------------
System Requirement
-----------------------
                  - Composer - 2
                  - Php 7.4
                  - Elastic Search - 7.9
                  - Mysql - 5.7
                  - Apache - 2.4 ( i go through this )
                  - Nginx  - 1.8 





## Some Command
----------------
                      
                      
                        - sudo php bin/magento setup:upgrade
                        - bin/magento setup:di:compile
                        - bin/magento setup:static-content:deploy -f
                        - bin/magento indexer:reindex
                        - bin/magento cache:flush
                        - bin/magento module:status 
                        - php bin/magento   - check when Namespace error
                        - php bin/magento setup:di:compile
                        - chmod -R 777 var/ pub/ generated/        
                        - sudo bin/magento module:disable Codilar_Thor   - Disable any Module
                        - rm -rf FolderName   - To Remove any Folder 
                        
                        
                        

















COMMAND
===============
- sudo su
- cat /etc/*release
- sudo apt-get update
- 




PHP
========
- php --version
- sudo apt autoremove
- sudo apt install php7.4
- sudo apt install php7.4-common php7.4-mysql php7.4 php7.4-cgi libapache2-mod-php7.4 php-pear php7.4-mbstring
- 


COMPOSER
==============
- composer -v
- - cd
                - pwd
                - check the php must be install
                - sudo apt install unzip
                - curl -sS https://getcomposer.org/installer -o composer-setup.php
                - sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
                - composer --- check the version


MYSQL
=========
Check the Mysql 
-----------------
- sudo service mysql status
- sudo service mysql stop
- sudo service mysql start
- mysql --version

Un-Install Mysql
=================
- sudo systemctl stop mysql
- sudo apt-get purge mysql-server mysql-client mysql-common mysql-server-core-* mysql-client-core-*
- sudo apt-get remove --purge mysql*
- sudo apt autoremove
- sudo apt-get autoclean
- sudo rm -rf /var/lib/mysql
- sudo rm -rf /etc/mysql



INSTALL MYSQL - 5.7 OR ORTHER VERSION ON UBUNTU 20.04 OR 18.04
==================================================================

STEP NEED TO INSTALL MYSQL
---------------------------

- sudo apt policy mysql-server      - check the version or any mysql is present in your system




INSTALL MYSQL - 8.0 OR OTHER VERSION ON UBUNTU 20.04  OR 18.04 
===============================================================
- 




APACHE
=========
- sudo apt install apache2
- sudo service apache2 start
- sudo service apache2 status
- sudo service apache2 stop
- systemctl status apache2.service
-  sudo systemctl enable apache2.service
- sudo nano /etc/apache2/sites-available/magento2.conf
- apache2 -v
- sudo a2enmod rewrite
- 

Un-INSTALL APACHE
===================
- Stop the apache - sudo service apache2 stop
- Remove apache
                  - sudo apt-get purge apache2 apache2-utils apache2.2-bin apache2-common
                     //or 
                  - sudo apt-get purge apache2 apache2-utils apache2-bin apache2.2-common
                  
                   //or 
                   - sudo apt-get purge apache2 apache2-utils apache2.2-bin apache2-common
                   - sudo apt-get autoremove
                   - sudo rm -rf /etc/apache2  
                   - whereis apache2   - check the if furthur exist after uninstall



INSTALL APACHE2
================
    
                 - 
                   
                   



NGINX
==========
- /etc/init.d/nginx status
- /etc/init.d/nginx stop
- /etc/init.d/nginx start
- nginx -v
- sudo nano /etc/nginx/sites-available/default   - check the port and which version php used by nginx
- 
- /etc/init.d/nginx stop
- 



ELASTIC 
==========

               - service elasticsearch status
               - 








Lets disable php 7.2 for apache and enable php 7.4 for Apache
-------------------------------------------------------------------------------------------------------
         - sudo a2dismod php7.2
         - sudo a2enmod php7.4
         - sudo service php7.3-fpm status
         - sudo service php7.3-fpm stop
         - sudo service php7.3-fpm start
         - sudo service php7.4-fpm status
         - sudo service php7.4-fpm stop
         







        Install Mysql 5.7
        ----------------------
               - sudo apt-cache policy mysql-server
               - sudo apt install -f mysql-client=5.7* mysql-community-server=5.7* mysql-server=5.7*
               - sudo mysql_secure_installation
               - Provide some  Details
               - 
               
               - mysql -u root -p12345678
               - show databases;
               - create database magento;
               - select *from core_data_config;
               - CREATE USER 'magento237'@'localhost' IDENTIFIED BY 'password';     - give proper password like - Sanjay1997@@ etc 
               - GRANT ALL PRIVILEGES ON *.* TO 'magento237'@'localhost' WITH GRANT OPTION;
               - bin/magento setup:install  --base-url=http://magento237.local/  --db-host=localhost  --db-name=magento  --db-user=magento237  --db-password=Sanjay1997@@ --backend-frontname=admin  --admin-firstname=admin  --admin-lastname=admin  --admin-email=devops1@codilar.com  --admin-user=admin1  --admin-password=admin123  --language=en_US  --currency=INR  --timezone=Asia/Kolkata  --use-rewrites=1
               - 
               




        Installl Composer if You Have Already Composer Version
        ----------------------------------------------------------
                    - cd
                    - pwd
                    - check the php must be install
                    - sudo apt install unzip
                    - curl -sS https://getcomposer.org/installer -o composer-setup.php
                    - sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
                    - composer --- check the version
                    -  /etc/nginx/sites-available/magento2
                    
                    

      Install Magento 
      ---------------------
      - Go To Directory of var/www/html   --> Inside this directory create one folder as per your wise like ( Magento237 )
      
                   - sudo mkdir Magento237  (Create the folder via Terminal Command )     also for delete - rm  -rf folderName
                   - cd Magento237/
                   - sudo su          (as super user mode )
                   
      - composer create-project --repository=https://repo.magento.com/ magento/project-community-edition Magento237
      
      (or)
      
      - composer create-project --repository=https://repo.magento.com/ magento/project-community-edition:2.3.7 Magento237
      
      
      - composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition:2.3.7-p1 .
      
      
     - Enter Magento Website(marketplace.magento.com) (Your  Created  Account  Access Key Under Myprofile Section (Public Key - Username & Password - Private Key)
      
      - 
      
      
      
      



### Error Occour Time Of Setup
----------------------------------
#### 1) [InvalidArgumentException]                                                       
  Could not find package magento/project-community-edition with version 2.3.7-p1. 
  
  Solution
  -----------
                       - Syntax error
                       
  
  
  
  
#### 2) Your requirements could not be resolved to an installable set of packages.
Problem 1
    - Root composer.json requires magento/product-community-edition 2.3.7 -> satisfiable by magento/product-community-edition[2.3.7].
    - magento/product-community-edition 2.3.7 requires ext-curl * -> it is missing from your system. Install or enable PHP's curl extension.
  Problem 2
    - phpunit/phpunit[9.0.0, ..., 9.5.7] require ext-dom * -> it is missing from your system. Install or enable PHP's dom extension.
    - Root composer.json requires phpunit/phpunit ^9 -> satisfiable by phpunit/phpunit[9.0.0, ..., 9.5.7].

To enable extensions, verify that they are enabled in your .ini files:
    - /etc/php/7.4/cli/php.ini
    - /etc/php/7.4/cli/conf.d/10-opcache.ini
    - /etc/php/7.4/cli/conf.d/10-pdo.ini
    - /etc/php/7.4/cli/conf.d/20-calendar.ini
    - /etc/php/7.4/cli/conf.d/20-ctype.ini
    - /etc/php/7.4/cli/conf.d/20-exif.ini
    - /etc/php/7.4/cli/conf.d/20-ffi.ini
    - /etc/php/7.4/cli/conf.d/20-fileinfo.ini
    - /etc/php/7.4/cli/conf.d/20-ftp.ini
    - /etc/php/7.4/cli/conf.d/20-gettext.ini
    - /etc/php/7.4/cli/conf.d/20-iconv.ini
    - /etc/php/7.4/cli/conf.d/20-json.ini
    - /etc/php/7.4/cli/conf.d/20-phar.ini
    - /etc/php/7.4/cli/conf.d/20-posix.ini
    - /etc/php/7.4/cli/conf.d/20-readline.ini
    - /etc/php/7.4/cli/conf.d/20-shmop.ini
    - /etc/php/7.4/cli/conf.d/20-sockets.ini
    - /etc/php/7.4/cli/conf.d/20-sysvmsg.ini
    - /etc/php/7.4/cli/conf.d/20-sysvsem.ini
    - /etc/php/7.4/cli/conf.d/20-sysvshm.ini
    - /etc/php/7.4/cli/conf.d/20-tokenizer.ini
You can also run `php --ini` inside terminal to see which files are used by PHP in CLI mode.


Solution
------------
     
        -   sudo dpkg --configure -a
        


## 3)This site can’t be reachedCheck if there is a typo in test.local. DNS_PROBE_FINISHED_NXDOMAIN
---------------------------------------------------------------------------------------------------------



  
  
  
  



