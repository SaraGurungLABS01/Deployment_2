# Purpose
The primary objective is to showcase the process of setting up a continuous integration by running a Jenkins build and performing a manual deployment to AWS Elastic Beanstalk. The focus is on demonstrating the setup and execution of the pipeline, integrating Jenkins, and deploying a Python URL shortening application to AWS Elastic Beanstalk. This process involves creating a zip artifact through Jenkins and then manually deploying it to Elastic Beanstalk.

## STEPS:

## 1. Starting a new Repository
1. Created a new Repository under the name Deployment_2
2. Downloaded the zip files from the Repository : C4_deployment-2 and unzipped them
3. Uploaded the unzipped files to the new repository that was created

## 2. Steps for Launching an EC2 with Jenkins installed and activated
1. Launch a new EC2 to install Jenkins with required plugins and python
2. Add Jenkins Repository: ``sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' ''
3. Update Package Information: "sudo apt update"
4. Install Jenkins: "sudo apt install jenkins"
5. Access Initial Admin Password: "sudo cat /var/lib/jenkins/secrets/initialAdminPassword"
6. Access Jenkins Web Interface: http://107.23.208.215:8080
7. Enter the initial admin password and follow the setup wizard.
8. Installed python through the terminal and downloaded and installed the Jenkins plugin "Pipeline Utility Steps"
9. Run Pipeline:
   -Create a new Jenkins job of type "Pipeline" and linked it to my repository.
   -Jenkins will automatically detect changes and run the pipeline.
10. Monitor Pipeline:
   -An output zip file is being packaged
![7AA15463-74FC-49F4-B0D8-0B4C00B366B8](https://github.com/SaraGurungLABS01/Deployment_2/assets/140760966/603e75b5-02d0-4f54-83be-1522cd51885c)

    

## Extracting the Zip file from Jenkins
#### Creating an SSH Tunnel for File Transfer
To securely transfer files from a remote server to a local machine, I utilized the scp command while establishing an SSH tunnel. Here's a brief overview of the process

1. Secure Copy (scp) Command:
Using the scp command in the terminal, I initiated the file transfer. By providing the necessary remote server details and file paths, I seamlessly copied the designated file to my local machine.

2. SSH Tunnel Establishment:
Prior to the file transfer, I established an SSH tunnel between my local machine and the remote server. This ensured the security of the data in transit and enabled a protected channel for the file transfer.

3. Successful Transfer:
The scp command executed successfully, and the file was transferred from the remote server to my local machine through the established SSH tunnel. The transferred file was saved to the designated local Download folder.

![6A3A227D-9F96-4DCD-BC1F-4B72610DC853](https://github.com/SaraGurungLABS01/Deployment_2/assets/140760966/0353a742-44eb-4872-8956-65f76c864257)

## Proceeding to Next steps

1. Accessing AWS Console and Elastic Beanstalk:
   - Opened the AWS Management Console.
   - Navigated to the Elastic Beanstalk service.
     
2. Creating an Application:
   - Selected the option to create a new application.
     
3. Configuring Application Details:
   -Chose the desired platform for the application: Python 3.9 running on 64bit Amazon Linux 2023.

4. Uploading Application Code:
  - Under the "Application code" section, selected the "Upload" option.
  - Specified the local file for deployment, denoting it as "Version: v1".
  -    Uploaded the previously generated zip file artifact containing the application files.
    
5. Setting EC2 Instance Profile:
   -Set the EC2 instance profile to "Elastic-EC2". This profile configuration ensures appropriate permissions for the instances in the Elastic Beanstalk environment.

6. Defining VPC and Availability Zone:
   - Utilized the default Virtual Private Cloud (VPC) for deployment.
   - Chose the availability zone: us-east-1a.
  
7.Configuring Root Volume: 
   - Selected "General Purpose (SSD)" as the root volume type.
   - Specified a size of 10GB for the root volume.

By meticulously following these steps, I successfully deployed the application to AWS Elastic Beanstalk. This deployment not only ensured the smooth execution of the application but also benefited from the flexible and managed environment provided by Elastic Beanstalk, allowing for efficient scaling and easy management.





![86C96B3A-D374-4601-851E-DF5EAF66504D_1_201_a](https://github.com/SaraGurungLABS01/Deployment_2/assets/140760966/906490c5-944c-48a1-baca-83f13938aa84)




![431C58EC-DF5F-4B36-B3ED-D786DB15C74D_1_201_a](https://github.com/SaraGurungLABS01/Deployment_2/assets/140760966/f028250d-a5ed-4d0a-a233-2fa60a4c04fb)









## System Diagram 



![Deployment 2](https://github.com/SaraGurungLABS01/Deployment_2/assets/140760966/5d70cce1-03a2-4424-ab16-fd95c1302c80)


## Issues
 
None

## Optimization

Inorder to enhance efficiency, reliability, and security across the deployment pipeline and application, we can consider automating the artifact storage during the software development lifecycle without manual intervention. 
Additinally we can work on security enhancement by following the principle of least privilege and priortize security by implementing best practices such as encryption of data.

