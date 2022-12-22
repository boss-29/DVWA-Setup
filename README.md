# DVWA-Setup
## Installing and Setting up of DVWA/Damn Vulnerable Web Application
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
I will use boss as username and word as password
Save and Exit


