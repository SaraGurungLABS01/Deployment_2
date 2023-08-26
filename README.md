# Purpose

## Steps for Launching an EC2 with Jenkins installed and activated
1. Launch a new EC2 to install Jenkins with required plugins and python
2. Add Jenkins Repository: ``sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' ''
3. Update Package Information: sudo apt update4. 4. Step 1
4. Install Jenkins: sudo apt install jenkins
5. Access Initial Admin Password: sudo cat /var/lib/jenkins/secrets/initialAdminPassword
6. Access Jenkins Web Interface: [](http://107.23.208.215:8080)
7. Enter the initial admin password and follow the setup wizard.
8. Installed python through the terminal and downloaded and installed the Jenkins plugin "Pipeline Utility Steps"
9. Run Pipeline:
   -Create a new Jenkins job of type "Pipeline" and linked it to my repository.
   -Jenkins will automatically detect changes and run the pipeline.
10. Monitor Pipeline:
    -
12.  **Bold Text**
#### Header 4
1. Bullet number
2. Bullet number
    ##### Header 5
    - bullet point 
    - bullet point 

## Header 2 
Text [click here for image](https://github.com/kura-labs-org/Template/blob/main/Images/Screenshot%20(92).png)

## System Diagram 
![image](https://github.com/kura-labs-org/Template/blob/main/Images/26-1.jpeg)

## Header 2  
For more markdown syntax: https://www.markdownguide.org/cheat-sheet/
