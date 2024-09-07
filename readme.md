# SDLC Project: CI-CD Pipeline Submission

## Task 1: Set Up a Simple HTML Project. 
Create a simple HTML project and push it to a GitHub repository. 
#### Solution 1:
The link to the simple HTML project is as follows: [solution](https://github.com/vishwesh5544/devops-cicd)

## Task 2: Set Up an AWS EC2/Local Linux Instance with Nginx
#### Solution 2:
The app is deployed on my local machine's Nginx as my device is running [Pop!_OS](https://pop.system76.com/).
The nginx reverse proxy config is as follows:
```
server {
    listen 80;
    server_name awesomeweb;

    root /var/www/html/awesomeweb;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```
The deployment file structure is follows:

      /var/
       ├── www/
       │   ├── html/

Upon running the `tree` command the ouput is as follows:
![image](https://github.com/user-attachments/assets/cbc2d503-a003-4873-963b-e7e9bcf88f42)

Finally, the output on browser is as follows:
![image](https://github.com/user-attachments/assets/7eac2dd7-7cb1-4e3b-a3d1-ab977bd3b744)

## Task 3: Write a Python Script to Check for New Commits
Create a Python script to check for new commits using the GitHub API.
#### Solution 3:
I have create a python application using OOP Concepts using 

