#!/bin/bash
yum update -y
yum install -y
yum install -y httpd
wget https://github.com/ekene/xmen/archive/refs/heads/main.zip
unzip main.zip
cp -r xmen-main/* /var/www/html/
rm -rf main.zip xmen-main
systemctl enable httpd
systemctl start httpd
