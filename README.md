# DVWA-Setup
## Installing and Setting up of DVWA/Damn Vulnerable Web Application
![index](https://user-images.githubusercontent.com/96311735/209383424-a2c7b760-fe25-4fed-b2fd-01a302ecee73.jpeg)


Damn Vulnerable Web Application (DVWA) is a vulnerable web application used by penetration tester, ethical hacker and security enthusiast to practice and learn different vulnerable meathods. It involve various common vulnerable web application with diffrent difficulties levels and simple interface.

So let's dive into its installation process
Special Mention : https://github.com/ethicalhack3r/DVWA

The first step is to install git clone on your OS
```
apt install git
```
Then, clone DVWA to localhost files at **/var/www/html/**

```
git clone https://github.com/ethicalhack3r/DVWA
```

Rename the file to "dvwa" to remove later hassel by
```
mv DVWA dvwa
```
Give necessary permission
```
chmod -R 777 dvwa/
```
Config file 
```
cd dvwa/config
```
Copy the php file from default file 
```
cp config.inc.php.dist config.inc.php
```
Edit the php file with your username and password
```
vim config.inc.php
```
I will use "boss" as username and "word" as password.Save and Exit

Start MySql
```
service mysql start
```

Login in mysql
```
mysql -u root -p
```

Add new user in database on localhost server
```
create user 'boss'@'127.0.0.1' identified by 'word';
```

Grant all the necessary permission
```
grant all privileges on dvwa.* to 'boss'@'127.0.0.1' identified by 'word';
```

Save and Exit mysql and now we need to configure apache2
Path may change according to your apache version
```
cd /etc/php/7.4/apache2
```
```
vim php.ini 
```
In the php.ini file we need to change ***allow_url_fopen*** and ***allow_url_include*** value to **"on"**

Save and Exit

Restart apache services
```
service apache2 start
```
Now let's open the browser and navigate to **127.0.0.1/dvwa/** a setup page will appear, scroll down to the bottom and click on **"Create/Reset Database"**. Then it will create and configure the database and will be redirected to DVWA login page.

The default login is
**Username- admin Password- password**

The DVWA main page will appear with General Instruction and Warnings
In the DVWA Security we can find the diffrent difficulty levels you can set according to your need
