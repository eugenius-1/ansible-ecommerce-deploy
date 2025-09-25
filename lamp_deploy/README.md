This playbook is based on:
https://github.com/ansible/ansible-examples/tree/master/lamp_simple_rhel7

Remember to set innodb buffer pool size low to reduce memory consumption if required

## Tasks:

#### Common Task
1. Install Dependencies: python3-libselinux, python3-libsemanage, firewalld

#### DB Tasks
1. Install MariaDB Packages
2. Configure MySQL Configuration File
3. Create MariaDB LogFiles
4. Create MariaDB PID Directories
5. Restart MariaDB
6. Start Firewalld Service
7. Add Firewalld rule
8. Create Application Database
9. Create Application Database User

#### Web Tasks
1. Install httpd and PHP dependencies
2. Install git for downloading source code
3. Install firewalld
4. Start firewalld status
5. Add firewalld rule
6. Start httpd service
7. Download source code from repo
8. Create index.php file from template.