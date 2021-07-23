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


        Install Mysql 5.7
        ----------------------
               - sudo apt-cache policy mysql-server
               - sudo apt install -f mysql-client=5.7* mysql-community-server=5.7* mysql-server=5.7*
               - sudo mysql_secure_installation
               - Provide some  Details
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
                    

      Install Magento 
      ---------------------
      - Go To Directory of var/www/html   --> Inside this directory create one folder as per your wise like ( Magento237 )
      
                   - sudo mkdir Magento237  (Create the folder via Terminal Command )     also for delete - rm  -rf folderName
                   - cd Magento237/
                   - sudo su          (as super user mode )
                   
      - composer create-project --repository=https://repo.magento.com/ magento/project-community-edition Magento237
      
      (or)
      
      - composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition:2.3.7-p1 .
      
      
     - Enter Magento Website(marketplace.magento.com) (Your  Created  Account  Access Key Under Myprofile Section (Public Key - Username & Password - Private Key)
      
      - 
      
      
      
      



### Error Occour Time Of Setup
----------------------------------
1) [InvalidArgumentException]                                                       
  Could not find package magento/project-community-edition with version 2.3.7-p1. 
  
  
  
2) Your requirements could not be resolved to an installable set of packages.

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


3)


  
  
  
  



