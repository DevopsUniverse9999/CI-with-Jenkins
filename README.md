# CI-with-Jenkins
![CI](https://user-images.githubusercontent.com/122671107/212466615-6abe9a79-8608-425f-8bde-4eae53c513b5.png)

# Setting up the Jenkins Server

=>sudo yum install wget -y
=>sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum upgrade -y
# Add required dependencies for the jenkins package
sudo yum install java-11-openjdk -y
sudo yum install jenkins -y
sudo systemctl daemon-reload
start jenkins
# You can enable the Jenkins service to start at boot with the command:
sudo systemctl enable jenkins
# You can start the Jenkins service with the command:=
sudo systemctl start jenkins
# You can check the status of the Jenkins service using the command:
sudo systemctl status jenkins
sudo su - ec2-user
# echo "echo of jenkins installation"
==============================================
============== Notice Important =============
after installed Jenkins make sure to vi /etc/passwd
=> and change :/var/lib/jenkins:bin/bash
After intallation switch su - to be jenkins users . 

# Configuartion of Jenkins Server
then write the cat and the code which is been shown while loginf jenkins 
Ex:- cat (jenkins ...)
then write
sudo su 
vi /etc/passwd
then go to the last line and change the false to bash 
(save and exit --> :w and :qa)
su - jenkins (u will directely go into jenkins allined path )
exit 
visudo 
then 

# Use which java to know the position of java 

su - jenkins 
exit 
visudo 
then then take the curser down by pressing the down arrow button till %wheel ALL=(ALL)  ALL
add 
jenkins ALL=(ALL) NOPASSWD:ALL 

whoami -------------->to know the companenet u are using 

sudo yum install git


sudo vi etc/passwd :- modify the credencials and motify jenkins user 
change the false --> bash

sudo vi /etc/sudoers 
and then put under % while
jenkins ALL=(ALL)   Nopasswd=none 

---------------------------maven plugin----------------
manage jenkins --> manage plugin ---->  Install plugin ---> maven Installer 

----------------------------------to configure maven -------------------
manage jenkins => global tools configuration =>click on the maven installer =>provide the name => select the version click on the save & Apply

click on the new item
provide the name of the new item and select the maven project 
click on add
source code managenet --->click on GIT---> provide the git instance (URL of github project)
go to post steps---->click on add--->Invoke top-level Maven targets--->select the maven from drop down
In goals write clean 
save & apply
build

