<h1>Setting Up Jenkins Master & Slave</h1>

<h2>Prerequisites</h2>

- Any Operating System (Ubuntu)
- Network Access from Jenkins Master Server
- Java, JRE, JDK
- New User
- Directory with User Ownership
- Tools Required (Maven, Ant, Git)

# STEPS
Setting up the Jenkins Master & Slave 

Step 1: Launch EC2 Instance on AWS
![A](https://user-images.githubusercontent.com/52894481/188257251-e37f2af4-d0df-456c-8fef-9b911d7435f2.JPG)

Step 2: Set up Security Group

Step 3: Run the command below: 
command:apt update && apt install openjdk-8-jdk -y

Step 5: Create new User with Home Directory & password
command: adduser devops 
command: passwd devops

Step 6: Create Directory 
mkdir mkdir /opt/jenkins-slave

Step 7: Change Ownership 
Command: chown devops.devops /opt/jenkins-slave/ -R
 
Step 7: Enable password authentication
Command: vim /etc/ssh/sshd_config

![B](https://user-images.githubusercontent.com/52894481/188257284-918022d5-1033-4041-ab52-b57bfc5aa5b7.JPG)

Step 8: restart ssh service for changes to take effect
Command: systemctl restart sshd
 
Step 9: log on to jenkins server

Step 10: Create a new node(Manage Jenkins > Create new node)

Step 11: Update Security Group on AWS to permit Jenkins server to ssh to Node
![C](https://user-images.githubusercontent.com/52894481/188257312-09be445e-a95c-4386-9c87-fbdfd12072e9.JPG)

Step 12: Set log in credentials on Jenkins to log in via ssh
![D](https://user-images.githubusercontent.com/52894481/188257323-ccac5eba-6c74-462f-aea8-02aa5c592a90.JPG)

Step 13: Launch Node 
![F](https://user-images.githubusercontent.com/52894481/188257335-18545f80-5d66-40a3-b718-6180b3105baf.JPG)
