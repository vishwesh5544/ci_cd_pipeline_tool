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

## Combined: Task 3 + Task 4
- **Task 3 - Write a Python Script to Check for New Commits**: Create a Python script to check for new commits using the GitHub API.
- **Task 4 - Write a Bash Script to Deploy the Code**: Create a bash script to clone the latest code and restart Nginx.
#### Comined Solution:
I have create a python application using OOP Concepts to achieve reusability and readibility of code. 

The link to the python solution: [Solution](https://github.com/vishwesh5544/vish_commit_checker)

## Task 5: Set Up a Cron Job to Run the Python Script
Create a cron job to run the Python script at regular intervals.
#### Solution 5:
1. Making the python tool script executable
`chmod +x <path-to-python-repo>/*`
2. Setting up the crontab using `crontab -e` is as follows:
![image](https://github.com/user-attachments/assets/3498a358-2411-41be-9736-3783403f7b9c)
3. Crontab log is as follows:
![image](https://github.com/user-attachments/assets/67ce162c-baa0-421d-a6df-beeab56780d0)
4. (EXTRA POINT) I logged cron output to a file in home directory. Let's tail and see the output of running script:
![image](https://github.com/user-attachments/assets/c021a6da-7552-48f2-8394-8bddc014d280)

## Task 6: Test the Setup 
Make a new commit to the GitHub repository and check that the changes are automatically deployed.



