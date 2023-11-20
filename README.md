# Original version of the project 

MyShuttle is a sample Java/JEE application that provides booking system, admin portal and a control system for the drivers. The application uses entirely open source software including Linux, Java, Apache, and MySQL which creates a web front end, an order service, and an integration service.

![](https://vstsdemodata.visualstudio.com/aa2f337f-2dbf-4700-88e5-bf4f57f49cc6/_api/_versioncontrol/itemContent?repositoryId=14c9c1ce-2de9-4198-a252-3caca0305407&path=%2F1.png&version=GBmaster&contentOnly=true&__v=5)

# Updated version of the project using  AWS

- Set Up and configure Jenkins/Sonarqube/Nexus servers on EC2 instance (t2.medium)
- Install java 8 or java 11


- Jenkins/Github integration

Configure Github credentials in jenkins UI 
Create a webhook in Github and paste jenkins URL

- Jenkins/Maven Integration

Install Maven Integration pluggin
Configure MAven in global tool configuration on Jenkins UI

- Jenkins/Nexus Integration

Add Nexus credentials in maven in Jenkins server: in server tag
#sudo vi  /var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/maven3.8.6/conf

Configure Nexus repo URL in pom.xml using distribution management tag

- Jenkins/Sonarqube Integration

Start Sonarqube as sonar user

To start sonarqube:
#sh /opt/sonarqube/bin/linux-x86-64/sonar.sh start

Configure Sonarqube URL details in pom.xml in properties tag


- To automate task create a JenkinsFile in project repo

# Coming Soon

Step by step approach on how to successfully build a Jenkins CI pipeline for this project.