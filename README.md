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


## Some Command For Magento
----------------------------
                      
                      
                        - sudo php bin/magento setup:upgrade
                        - sudo bin/magento setup:di:compile
                        - sudo bin/magento setup:static-content:deploy -f
                        - sudo bin/magento indexer:reindex
                        - sudo bin/magento cache:flush
                        - sudo bin/magento cache:clean
                        - sudo bin/magento module:status 
                        - sudo php bin/magento   - check when Namespace error
                        - sudo php bin/magento setup:di:compile
                        - sudo chmod -R 777 var/ pub/ generated/        
                        - sudo bin/magento module:disable Codilar_Thor   - Disable any Module
                        - rm -rf FolderName   - To Remove any Folder 
                        - bin/magento dep:mod:show
                        - sudo bin/magento de:mo:se developer

COMMAND
===============
- sudo su
- cat /etc/*release
- sudo apt-get update
- sudo nano /etc/hosts
- unlink shopmonk
- sudo dpkg --configure -a
- cd
- pkexec chmod 555 /etc/sudoers
- pkexec chmod 555 /etc/sudoers.d/README  - if etc folder is worldwritable stage
- whereis
- rm -rf
- sudo a2enmod rewrite
- 
 
Lets disable php 7.2 for apache and enable php 7.4 for Apache
--------------------------------------------------------------
         - sudo a2dismod php7.2
         - sudo a2enmod php7.4
         - sudo service php7.3-fpm status
         - sudo service php7.3-fpm stop
         - sudo service php7.3-fpm start
         - sudo service php7.4-fpm status
         - sudo service php7.4-fpm stop
         
PHP INSTALL
===========
- php --version
- sudo apt install software-properties-common
- sudo add-apt-repository ppa:ondrej/php
- sudo apt-get update
- sudo apt install php7.4
- sudo apt install php7.3
- sudo apt install php
- sudo apt-get install php7.4-common php7.4-xml php7.4-curl php7.4-bcmath php7.4-intl php7.4-gd php7.4-zip php7.4-mysql php7.4-soap php7.4-mbstring
- sudo apt install php7.4-common php7.4-mysql php7.4 php7.4-cgi libapache2-mod-php7.4 php-pear php7.4-mbstring
- sudo apt-get install -y php7.4 libapache2-mod-php7.4 php7.4-common php7.4-gd php7.4-mysql php7.4-curl php7.4-intl php7.4-xsl php7.4-mbstring php7.4-zip php7.4-bcmath php7.4-iconv php7.4-soap php7.4--fpm
- ext-bcmath,ext-ctype,ext-curl,ext-dom,ext-gd,ext-hash,ext-iconv,ext-int,ext-mbstring,ext-openssl,ext-pdo_mysql,ext-simplexml,ext-soap,ext-xsl, ext-zip, ext-  sockets
 
- To switch that to the newer 7.1,7.2,7.3,7.4 version, first disable older PHP version:
     - user@test:~# sudo a2dismod php7.0(select your version)


UN-INSTALL PHP
==============
                 - sudo apt-get purge php7.*
                 - sudo apt-get autoclean
                 - sudo apt-get autoremove
                 - sudo apt autoremove


COMPOSER
==============
                - composer -v
                - cd
                - pwd
                - check the php must be install
                - sudo apt install unzip
                - curl -sS https://getcomposer.org/installer -o composer-setup.php
                - sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
                - composer --- check the version

UN-INSTALL COMPOSER
====================
                       - 
                       - 


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

- SELECT user,authentication_string,plugin,host FROM mysql.user;
- 

STEP NEED TO INSTALL MYSQL
---------------------------
                    -    sudo apt policy mysql-server      - check the version or any mysql is present in your system
                    -    sudo apt update
                    -    sudo apt install wget -y
                    -    wget https://dev.mysql.com/get/mysql-apt-config_0.8.12-1_all.deb
                            Once downloaded, install the repository by running the command below:
                    -    sudo dpkg -i mysql-apt-config_0.8.12-1_all.deb




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

Un-INSTALL APACHE
===================
- Stop the apache                - sudo service apache2 stop
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

sudo apt update
sudo apt install nginx
After installing Nginx, the commands below can be used to stop, start and enable Nginx service to always start up with the server boots.

sudo systemctl stop nginx.service
sudo systemctl start nginx.service
sudo systemctl enable nginx.service

- /etc/init.d/nginx status
- /etc/init.d/nginx stop
- /etc/init.d/nginx start
- nginx -v
- sudo nano /etc/nginx/sites-available/default   - check the port and which version php used by nginx
- 
- /etc/init.d/nginx stop
- systemctl enable nginx
- nginx -t
- systemctl restart nginx   -------- if any error get when test then run below cmd
- tail -f /var/log/nginx/error.log
- ps auxf | grep nginx
- chown -R www-data:www-data /var/www/yourdomain.com
- netstat -plant | grep '80\|443'
- ufw status


Un Install NGINX
===================
    - sudo apt-get remove nginx nginx-common
    - sudo apt-get purge nginx nginx-common
    - sudo apt-get autoremove
    



ELASTIC 
==========

               - service elasticsearch status
               - /etc/init.d/elasticsearch status
               - /etc/init.d/elasticsearch start
               - /etc/init.d/elasticsearch stop
               - /etc/init.d/elasticsearch restart
               - /etc/init.d/elasticsearch force-reload
           
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
               - select *from magento;   - use your database
               - select *from core_config_data;
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
                    -  etc/nginx/sites-available/magento237  - open a nano file paste below command
                    
                    -                    upstream fastcgi_backend {
                                           server unix:/run/php/php7.4-fpm.sock;
                                         } 

                                         server {
                                                 listen:80;
                                                 listen [::]:80;
 
                                                 set $MAGE_ROOT /var/www/html/magento237;
                                                 include /var/www/html/magento237/nginx.conf.sample;

                                                 server_name magento237.local;

                                         }



                         Inside html/Folder
                         ===================
                              - cd /etc/nginx/sites-available/  - check the default page of nginx 
                              - cd /etc/nginx/sites-enabled/   - ls - check which site is enable
                            
                          Base Root 
                          =========
                              - sudo ln -s /etc/nginx/sites-available/magento237 /etc/nginx/sites-enabled
                              - 


      Install Magento 
      ---------------------
      - Go To Directory of var/www/html   --> Inside this directory create one folder as per your wise like ( Magento237 )
      
                   - sudo mkdir Magento237  (Create the folder via Terminal Command )     also for delete - rm  -rf folderName
                   - cd Magento237/
                   - sudo su          (as super user mode )
                   
      - composer create-project --repository=https://repo.magento.com/ magento/project-community-edition Magento237
      
      (or)
      
      - composer create-project --repository=https://repo.magento.com/ magento/project-community-edition:2.3.7 Magento237(you folder name)
      
      
      - composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition:2.3.7-p1 .
      
      
     - Enter Magento Website(marketplace.magento.com) (Your  Created  Account  Access Key Under Myprofile Section (Public Key - Username & Password - Private Key)
      
      - 
      
 
 
 #FINAL STEP FOR SETUP
 ======================
 
 STEP - 1) Install all the pre required dependency for magento install(Check from Official Site)
 --------------------------------------------------------------------------------------------------
                        - Install Apache or Nginx
                        - Install Mysql 
                        - Install Elasticsearch
                        - Install Php
                        - Install Curl
                        - Install Composer
                        
STEP - 2) 
========================================================================
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


## 4) nginx: [emerg] unknown directive "listen:80" in /etc/nginx/sites-enabled/magento237:6
nginx: configuration file /etc/nginx/nginx.conf test failed
---------------------------------------------------------------------



## 5) This page isn’t workinglocalhost is currently unable to handle this request.
HTTP ERROR 500
--------------------------------------------------------------------------------
Solution
-------------
                 - go to magento app/  directory and check the bootstrap.php file  -- un comment line 14 for see the error

  
  
## 6) Fatal error: Uncaught Zend_Cache_Exception: cache_dir "/var/www/html/magento/var/page_cache" is not writable in /var/www/html/magento/vendor/magento/zendframework1/library/Zend/Cache.php:209 Stack trace: #0 /var/www/html/magento/vendor/magento/zendframework1/library/Zend/Cache/Backend/File.php(180): Zend_Cache::throwException() #1 /var/www/html/magento/vendor/colinmollenhour/cache-backend-file/File.php(87): Zend_Cache_Backend_File->setCacheDir() #2 /var/www/html/magento/vendor/magento/zendframework1/library/Zend/Cache.php(153): Cm_Cache_Backend_File->__construct() #3 /var/www/html/magento/vendor/magento/zendframework1/library/Zend/Cache.php(94): Zend_Cache::_makeBackend() #4 /var/www/html/magento/vendor/magento/framework/App/Cache/Frontend/Factory.php(156): Zend_Cache::factory() #5 /var/www/html/magento/vendor/magento/framework/Cache/Frontend/Adapter/Zend.php(38): Magento\Framework\App\Cache\Frontend\Factory->Magento\Framework\App\Cache\Frontend\{closure}() #6 /var/www/html/magento/vendor/magento/framework/ObjectManager/F in /var/www/html/magento/vendor/magento/zendframework1/library/Zend/Cache.php on line 209
-------------------------------------------------------------------------------------------------------
Solution
-----------------
                           - 

  

## 7 ) Errors during compilation: AbstractConfigOption.php

Solution
----------
                    - composer require symfony/console=4.4.26  - run this command inside your var/www/html/magento$ directory

