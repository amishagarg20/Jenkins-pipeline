# Jenkins-pipeline
Build Docker Image Using Jenkins Pipeline &amp; Push to AWS ECR
Launch an EC2 instance and named as Master jenkins
Install jenkins, 
sudo yum update –y
Add Repo : sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
Import key file from Jenkin CI : sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum upgrade
Install Jenkins: sudo yum install jenkins java-1.8.0-openjdk-devel -y
sudo systemctl daemon-reload
Start jenkins as service: sudo systemctl start jenkins
Check jenkins Status : sudo systemctl status jenkins
--------------------------------------------------------------------------------------
Install Docker:
Install Package: sudo yum update -y
Install Docker engine: sudo amazon-linux-extras install docker
Start service: sudo service docker start
Add ec2 user to group : sudo usermod -a -G docker ec2-user
--------------------------------------------------------------------------------------
Add jenkins to docker group : sudo usermod -a -G docker jenkins
Restart jenkins service: service jenkins start
Reload daemon : sudo systemctl daemon-reload
Restart Docker service: sudo service docker restart
------------------------------------------------------------------------------------
On jenkins Install the docker plugins:
1) docker plug=in
2) Docker pipeline plug=in
---------------------------------------------------------------------------------------
Install Git: yum install Git
-------------------------------------------------------------------------------------
On AWS create on ECR repo .
Create IAM role with Amazon EC2 Container Registry Full access policy and attach the IAM policy with your EC2 instance.
---------------------------------------------------------------------------------------------------------------------
Create jenkins Pipeline with project name
Add your pipeline code
And click on build
now you can run your docker image on AWS ECS or eks anywhere.
