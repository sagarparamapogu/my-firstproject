JENKINS INSTALLATION
Jenkins Installation on an EC2 Instance.
1. Create an EC2 instance with size t2.medium.
2. Connect to EC2 instance and install jenkins using the commands  1.sudo apt update 2.sudo apt install maven 3.Then search for install jenkins in ubuntu and run the commands to       
   sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
   sudo apt-get install jenkinsian-stable/jenkins.io-2023.key
   echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
   https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
   /etc/apt/sources.list.d/jenkins.list > /dev/null
   sudo apt-get update
   sudo apt-get install jenkins
3. Check whether the Jenkins has been installed and running or not.
   sudo systemctl status jenkins
4. Make sure to open the 8080 port on your Instance SG.
5. Try connecting to the Jenkins using http://ip-address:8080
6. Get the Jenkins Password : sudo cat /var/lib/jenkins/secrets/initialAdminPassword

Trigger jenkins job with this text commit.
