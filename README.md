Shampooing
=============================


- [Networking](#networking)
- [Linux](#linux)
- [Docker](#docker)
- [Kubernetes](#kubernetes)
- [Python](#python)
- [Gitlab-ci](#gitlab-ci)
- [Vmware](#vmware)
- [Ansible](#ansible)
- [Terraform](#terraform)


----------------------------------

# Networking 
Understand/Answer the following:
* What is VLAN?
* What is VXLAN?
* What is default-gateway?
* DNS
* hosts file

# Linux 
Answer the following questions:
* known_hosts file  (fingerprint)
* authorized_keys file
* /etc/suduoers vs /etc/sudoers.d/
* /etc/shadow
* /etc/passwd
* Read about [Filesystem Hierarchy](https://linuxjourney.com/lesson/filesystem-hierarchy)
* inode
* what is the difference between symlink and hard link? 
* lvm
* mount command
* /etc/fstab
* lsblk command
* fork & exec
* setuid
* selinux

Tasks:
* Create VM from ISO on vSphere
* Set the following network configurations:
  * IPv4
  * DNS
  * Default gateway
* Install nmtui cli via package manager
* Change ip address again and than connect to server via ssh.
* Add epel repo
* install cowsay
* Create users 'daniel' & 'sahar'
* Add daniel sudo permissions
* Set daniel password to daniel
* Add sahar permissions rwx to /home/daniel/ (not with setfacl)
* Create via daniel the file /home/daniel/not-for-sahar and grant it permissions so sahar couldn't delete the file.
* Create on vsphere 3 disks (10gb each). 
* Mount 1 disk to /devops
* Use 1 disk to increase root-lv
* Use 1 disk to create new lv and mount to /ela
* Verify that the disks would be mounted after reboot.
* change selinux to permissive
* Bash script. The script should "logrotate" the files. For example the following folder:
* for all "log" files:
  * if it end with number --> +1
  * else --> add "1"
* add new log file
    * before: 
    * /legendary-folder
      * good.log
      * good.log1
      * good.log2
      * bad.log
      * bad.log1
      * bad.log2
      * README
    * after:
    * /legendary-folder
      * good.log
      * good.log1
      * good.log2
      * good.log3
      * bad.log
      * bad.log1
      * bad.log2
      * bad.log3
      * README


# Docker 
* Read about: (Bonus)
  * Linux kernel namespaces
  * Control groups(cgroups)
  * Capabilities
* What are the pros for using docker multi-stage build?
* docker-compose

Task
* Install docker
* Create simple spring boot app
* Create multi-stage docker file to build image





# Kubernetes 
Udemy:
* [Kubernetes for beginners](https://www.udemy.com/course/learn-kubernetes/)
* [Certified Kubernetes Administrator](https://www.udemy.com/course/certified-kubernetes-administrator-with-practice-tests/)

Task:
* Install k3s
* deploy nginx deployment
* create NodePort svc
* 

# Python 
* Prime numbers
  * Create a python package that gets number(>=2) and returns 
* Goldbach conjecture
  * Create fastAPI/Flask app that has 2 routes:
    * /hello-world            # Returns "Hello World!"
    * /goldbach/<:number>     # Returns 2 prime numbers that their sum equals to input number
    * 

# Gitlab-ci 
Task 1:
* Create pipeline for spring boot app (docker)
* The pipeline will have the following stages:
  * tag
  * build and push image
  * run the image locally

Task 2:
* create 2 pipelines:
  * package:
    * tag - semVer tag, build only on master branch
    * test
    * build
    * push pypi package to artifactory
  * app:
    * tag - semVer tag, build only on dev branch and promote from dev to master
    * build & test & push
    * deploy on kubernetes 

# Vmware (Not Mandatory)
* Read about:
  * DRS
  * HA
  * vMotion
  * Snapshot (copy on write)
  * VM's files

# Ansible 
* Install ansible on your vm from Linux section
* create playbook that does the following:
  * Create vm from template
  * install httpd
  * open fw port 80
  * start and enable nginx service
  * allow ansible vm ssh to the new vm without password

# Terraform - TODO
 
