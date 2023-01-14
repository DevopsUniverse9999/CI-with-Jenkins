# CI-with-Jenkins
![CI](https://user-images.githubusercontent.com/122671107/212466615-6abe9a79-8608-425f-8bde-4eae53c513b5.png)

# Setting up the Jenkins Server

=>sudo yum install wget -y <br>
=>sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo <br>
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key <br>
sudo yum upgrade -y <br>
# Add required dependencies for the jenkins package
sudo yum install java-11-openjdk -y <br>
sudo yum install jenkins -y <br>
sudo systemctl daemon-reload <br>
start jenkins <br>
# You can enable the Jenkins service to start at boot with the command:
sudo systemctl enable jenkins
# You can start the Jenkins service with the command:=
sudo systemctl start jenkins <br>
# You can check the status of the Jenkins service using the command:
sudo systemctl status jenkins <br>
sudo su - ec2-user <br>
# echo "echo of jenkins installation"
==============================================
============== Notice Important =============
after installed Jenkins make sure to <br>
vi /etc/passwd <br>
change :/var/lib/jenkins:bin/bash <br>
After intallation switch su - to be jenkins users . <br>

# Configuartion of Jenkins Server
then write the cat and the code which is been shown while loginf jenkins <br> 
Ex:- cat (jenkins ...) <br>
then write <br>
sudo su <br>
vi /etc/passwd <br>
then go to the last line and change the false to bash <br>
(save and exit --> :w and :qa) <br>
su - jenkins (u will directely go into jenkins allined path ) <br>
exit <br>
visudo <br>
then <br>

# Use which java to know the position of java 

su - jenkins <br>
exit <br>
visudo <br>
then then take the curser down by pressing the down arrow button till %wheel ALL=(ALL)  ALL <br>
add <br>
jenkins ALL=(ALL) NOPASSWD:ALL  <br>

whoami -------------->to know the companenet u are using <br>

sudo yum install git <br>


sudo vi etc/passwd :- modify the credencials and motify jenkins user  <br>
change the false --> bash <br>

sudo vi /etc/sudoers <br>
and then put under % while <br>
jenkins ALL=(ALL)   Nopasswd=none <br> 

---------------------------maven plugin----------------
manage jenkins --> manage plugin ---->  Install plugin ---> maven Installer <br> 

----------------------------------to configure maven -------------------
manage jenkins => global tools configuration =>click on the maven installer =>provide the name => select the version click on the save & Apply <br>

click on the new item <br>
provide the name of the new item and select the maven project <br> 
click on add <br>
source code managenet --->click on GIT---> provide the git instance (URL of github project) <br>
go to post steps---->click on add--->Invoke top-level Maven targets--->select the maven from drop down <br>
In goals write clean <br>
save & apply <br>
build

