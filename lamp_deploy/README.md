This playbook is based on:
https://github.com/ansible/ansible-examples/tree/master/lamp_simple_rhel7

Remember to set innodb buffer pool size low to reduce memory consumption if required

## Tasks:

#### Pre Task (Establishing passwordless ssh connection between hosts)
1. Establish passwordless ssh connection between the ansible controller and the other 2 corresponding VMs by creating the ssh private key files specified in the inventory file with the command:
`ssh-keygen -t rsa -f <private_key_file>`
2. Distribute the associated public keys to the corresponding VMs by running the command:
`ssh-copy-id -i <private_key_file> <user>@<VM_hostname_or_IP>`
3. Test that passwordless ssh connectivity is successful between the ansible controller and corresponding VM host by running this command in the directory containing the inventory file:
`ansible -m ping -i inventory <inventory_hostname>`

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