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

