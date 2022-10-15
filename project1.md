# PROJECT 1: LAMP STACK IMPLEMENTATION
## WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS

A technology stack is a set of frameworks and tools used to develop a software product. 
This set of frameworks and tools are very specifically chosen to work together in creating a well-functioning software.

Step 1: Installing Apache

Command: sudo apt install apache2
![1](https://user-images.githubusercontent.com/105853738/195987298-c0ce67ae-aaac-4a0c-8136-5a4efbb03e8a.PNG)



Step 2: Installing Apache serverand updating the firewall

Commands:

sudo updating the firewall enable

sudo updating the firewall allow "Apache"
![2](https://user-images.githubusercontent.com/105853738/195987772-9a36854d-7268-4f96-92a0-024637a397b3.PNG)



Step 3: Install MySQL Server and Setup Root Password

Commands:

sudo apt install mysql-server


sudo mysql_secure_installation ![mysql stuff](https://user-images.githubusercontent.com/105853738/195989068-7b2054bb-84d0-4a0c-b9c6-df14b1212b47.PNG)



Step 4: Install PHP and Core Packages

Command: sudo apt install php libapache2-mod-php php-mysql
![php installation](https://user-images.githubusercontent.com/105853738/195989347-12812bcc-0b5f-48a4-a7c3-ac2f473a6452.PNG)



Step 5: Setup VirtualHost on Apache to Serve PHP

Commands:
sudo mkdir /var/www/projectlamp (Create project directory)

sudo chown -R $USER:$USER /var/www/projectlamp (Change user ownerships)

sudo vim /etc/apache2/sites-available/projectlamp.conf (Create Virtual Host conf for project)

sudo a2ensite projectlamp (Enable project)

sudo a2dissite 000-default (Disable default site)

sudo apache2ctl configtest (Test configurations)

sudo systemctl reload apache2 (Reload Apache2 service)
![lamp2](https://user-images.githubusercontent.com/105853738/195990574-57283a21-283a-4354-88a4-75ac8ffb2fa7.PNG)


Step 6: Enable PHP on the Website

Commands:
sudo vim /etc/apache2/mods-enabled/dir.conf (Edit dir.conf to place index.php at higher precedence)

vim /var/www/projectlamp/index.php (Create PHP index page)
![php finallly](https://user-images.githubusercontent.com/105853738/195991004-d91d7714-1d03-4793-bac9-8da2e4570d05.PNG)

