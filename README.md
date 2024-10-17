# Integrate Jenkins with Sonarqube,Git,Tomcat:
	First we need to create the 3 ec2 instance one for Jenkins,another for tomcat and one more instance(t2.medium taken for sonar instance) for sonarqube and open the port no.9000 for sonarqube server and 8080 for Jenkins,tomcat.

	Update the servers by using apt update -y command and install java on 3 servers.

	Install the Jenkins and maven on Jenkins server and install tomcat on tomcat server.

	On sonarqube instance we need to create user with the name of sonarqube by using adduser username command and swith to the sonarqube user by using su – username command.

	Install the sonarqube from binaries.sonarsource.com.

This is command
                Wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.2.0.49834.zip
	Install the unzip on sonarqube server and unzip by using unzip folder name command.

	Change the owner permission by using chown sonarqube:sonarqube filepath/filename -R command.

	Change the file permission by using chmod 777 filepath/filename -R command.

	Go to sonarqube folder and go to bin folder and go to linux-x86-64 folder .

	Start the sonar server by using sh sonar.sh start command and log into sonarqube server by using server i.p address with port no.9000

	Go to manage Jenkins > plugins > available plugins search for sonar scanner and install it and restart Jenkins.

	Log into  Jenkins server and go to manage Jenkins and go to system which is under system configuration section.

	Configure the sonarqube server with Jenkins like sonarqube server url,add the sonarqube token(for the token we can go to sonarqube server click on A and click on my account and enter the any name click on generate token will be generated copy this token and paste it on Jenkins credentials).

	Go to tools and serach for  sonarqubescanner installation option and click on add enter name and click on apply and save.

	Install the deploy to container plugin .

	Create the pipeline job and write the pipeline script or generate the script by using pipeline syntax option.

# Declarative pipeline script
 ![image](https://github.com/user-attachments/assets/89697683-4bce-4d2d-abda-bee80632eda8)

# Build is success
 
![image](https://github.com/user-attachments/assets/d40752d5-e2a3-4c51-848c-ca6b8bee3c67)

# Code analysis by sonarqube
 
 




![image](https://github.com/user-attachments/assets/cfb997f3-e7a1-42d3-9297-d3d26d2cdb04)


![image](https://github.com/user-attachments/assets/37518c1a-e30e-4e0d-bc98-73b13ecb38e5)

# Deploy on Tomcat 
 
![image](https://github.com/user-attachments/assets/f5d00920-98f3-42c1-89e5-480b36cc00d6)

