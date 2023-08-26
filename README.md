# Purpose

## Starting a new Repository
1. Created a new Repository under the name Deployment_2
2. Downloaded the zip files from the Repository : C4_deployment-2 and unzipped them
3. Uploaded the unzipped files to the new repository that was created

## Steps for Launching an EC2 with Jenkins installed and activated
1. Launch a new EC2 to install Jenkins with required plugins and python
2. Add Jenkins Repository: ``sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' ''
3. Update Package Information: sudo apt update4. 4. Step 1
4. Install Jenkins: sudo apt install jenkins
5. Access Initial Admin Password: sudo cat /var/lib/jenkins/secrets/initialAdminPassword
6. Access Jenkins Web Interface: http://107.23.208.215:8080
7. Enter the initial admin password and follow the setup wizard.
8. Installed python through the terminal and downloaded and installed the Jenkins plugin "Pipeline Utility Steps"
9. Run Pipeline:
   -Create a new Jenkins job of type "Pipeline" and linked it to my repository.
   -Jenkins will automatically detect changes and run the pipeline.
10. Monitor Pipeline:
   -An output zip file is being packaged
   -

#### Proceeding to Next steps
1. Proceeded to next steps to "Create and Deploy a Python URL Shortener on AWS Elastic Beanstalk"
2. Zipped the downloaded files and used it when deploying on AWS Elatic Beanstalk
3. After following the entire step, made sure the health is OK and clicked the domain name
4.Nothing broke and was was successfully running

5. ## Header 2 
Text [click here for image](https://github.com/kura-labs-org/Template/blob/main/Images/Screenshot%20(92).png)

## System Diagram 
![image](https://github.com/kura-labs-org/Template/blob/main/Images/26-1.jpeg)

