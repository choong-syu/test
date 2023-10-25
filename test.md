예제입니다.

```bash
#!/bin/bash
yum -y remove mariadb-libs
yum -y install httpd php mysql php-mysql wget 
systemctl enable httpd
cd /var/www/html
wget https://github.com/kimjaehyeon0314/test/raw/main/kakao.tar.gz -O kakao.tar.gz
tar -xvf kakao.tar.gz
mv /var/www/html/kakao/{index.php,get_user_list.php,add_user.php} /var/www/html/
rm /etc/selinux/config
mv /var/www/html/kakao/config /etc/selinux
setenforce 0
systemctl start httpd
```

```
#!/bin/bash
yum -y remove mariadb-libs
yum -y install httpd php mysql php-mysql wget 
systemctl enable httpd
cd /var/www/html
wget https://github.com/kimjaehyeon0314/test/raw/main/kakao.tar.gz -O kakao.tar.gz
tar -xvf kakao.tar.gz
mv /var/www/html/kakao/{index.php,get_user_list.php,add_user.php} /var/www/html/
rm /etc/selinux/config
mv /var/www/html/kakao/config /etc/selinux
setenforce 0
systemctl start httpd
```
