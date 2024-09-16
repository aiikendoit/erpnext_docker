INSTALLING ERPNEXT VIA DOCKER FOR BEGINNERS – A STEP-BY-STEP GUIDE

Installing ERPNext via Docker is a convenient way to set up the platform without needing to deal with complex dependencies and configurations. Below are highly simplified steps to guide you through the process, assuming you have no prior experience with Docker:

Prerequisites
Docker installed. If you haven’t installed docker, refer to my earlier article to install
Docker Compose
Step 1: Create a Directory
Create a directory: Choose a location on your Ubuntu system where you want to set up ERPNext. Open a terminal and run the following command to create a directory:

mkdir erpnext_docker

Navigate to the directory: Change your working directory to the newly created directory:

cd erpnext_docker

Step 2: Create a Docker Compose File
Create a Docker Compose file: Use a text editor (such as nano or vim) to create a new file named docker-compose.yml within the erpnext_docker directory:

nano docker-compose.yml

Paste the Docker Compose configuration: Copy and paste the contents of this Docker Compose configuration file into the docker-compose.yml file.

Save and exit: Save the changes with CTRL + O to the file and accept the prompt, and exit the text editor with CTRL + X

Step 3: Start ERPNext Containers
Start ERPNext containers: Execute the following command to start ERPNext containers using Docker Compose.

docker compose -p pwd -f docker-compose.yml up

Step 4: Access ERPNext
Open ERPNext: Once the containers are up and running, open your web browser and navigate to http://localhost:8080. You should see the ERPNext login page.

Login Credentials: The default username is Administrator, and the password is admin.

Step 5: Additional Operations
To STOP all containers run the below command

sudo docker stop $(sudo docker ps -q)

To START all containers, run the below command

docker start $(docker ps -a -q)

To DELETE all docker images, run the below command

sudo docker system prune --all --force --volumes

To execute an interactive shell inside a running Docker container, run the below command:

sudo docker exec -it <NAME> /bin/bash

Replace <NAME> with the ID or the name of your docker container.

Conclusion
In conclusion, deploying ERPNext via Docker offers a streamlined and efficient solution for users, especially those new to the process. By following the steps outlined in this guide, you’ve learned how to set up ERPNext on Ubuntu using Docker containers with ease. This method not only simplifies the installation process but also ensures scalability and flexibility for future updates and modifications. Embrace the power of Docker to unlock the full potential of ERPNext for your business needs.