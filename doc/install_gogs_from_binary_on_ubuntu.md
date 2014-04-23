### Binary install gogs on ubuntu 14.04 LTS

### create user and install denpendency
- sudo adduser git
- sudo apt-get update
- sudo apt-get upgrade
- sudo apt-get install git
- sudo apt-get install mysql-server

### create the database
- $mysql -u root -p
- mysql> SET GLOBAL storage_engine = 'InnoDB';
- mysql> CREATE DATABASE gogs CHARACTER SET utf8 COLLATE utf8_bin;
- mysql> GRANT ALL PRIVILEGES ON gogs.* TO 'root'@'localhost' IDENTIFIED BY 'password';
- mysql> FLUSH PRIVILEGES;
- mysql> QUIT

### install the gogs
- mkdir gogs
- cd gogs
- curl -L http://gobuild.io/github.com/gogits/gogs/v0.2.0/linux/amd64 -o v0.2.0.zip
- unzip v0.2.0.zip
- ./start.sh

> The up-to-date binary could be found at
> http://gobuild.io/download/github.com/gogits/gogs
