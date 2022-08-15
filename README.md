# update_PR_status_with_jenkins_build_status
update_PR_status_with_jenkins_build_status

Steps:
=======
1. Install and configure Jenkins
2. Install GitHub plugin
3. Generate github Personal access tokens
4. create secret key with the PAT generated in step 3
5. Configure Jenkins to access the Github Repo using the secret key
6. Create Jenkins Job
7. create webhook in github repo to trigger jenkins job 


**1. Install and configure Jenkins**

a. Install Java 

  sudo amazon-linux-extras enable corretto8 -y
  sudo yum install java-1.8.0-amazon-corretto* -y
  sudo alternatives --config java
 
b. Install Jenkins 

  sudo wget -O /etc/yum.repos.d/jenkins.repo     https://pkg.jenkins.io/redhat-stable/jenkins.repo
  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
  sudo yum upgrade
  sudo yum install jenkins -y
  sudo systemctl enable jenkins
  sudo systemctl start jenkins
  sudo systemctl status jenkins

Now you can access jenkins on http://host_ip:8080 address.
The initial admin password will be located at : "/var/lib/jenkins/secrets/initialAdminPassword"

Please proceed with the installed the suggested plugins.

**2. Install GitHub plugin**

IF you have proceed with the installed the suggested plugins during jenkins setup then it will be automatically there, else you need to goto Manage Jenkins --> Plugin Manager --> Available --> Search for GitHub plugin -->contnue with  "install without restart" option.

<img width="1007" alt="image" src="https://user-images.githubusercontent.com/74225291/184620382-a5342f42-0ef1-4cbc-b2b8-269ee2699756.png">

**3. Generate github Personal access tokens**

![image](https://user-images.githubusercontent.com/74225291/184621012-5a809495-4d7c-49d0-a74b-3c912706b444.png)

![image](https://user-images.githubusercontent.com/74225291/184621031-41429845-2eb4-4d9b-bed1-e1a1f1fe8b31.png)

![image](https://user-images.githubusercontent.com/74225291/184621097-89a131c4-bcd9-4029-b5a1-09b974ee71f0.png)

![image](https://user-images.githubusercontent.com/74225291/184621140-88af2d87-6a5a-4525-966e-274a95b216d8.png)


