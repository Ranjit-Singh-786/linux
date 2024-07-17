# linux
# linux
## Useful Linux Commands and Deployment Steps Using AWS

### Installing Local Packages

To install a local package (.deb file) on Ubuntu using `dpkg`:

```bash
sudo dpkg -i app_file_name.deb
Make sure you're in the directory where app_file_name.deb is located.

Installing Git
To install Git on Ubuntu:
sudo apt install git

Certainly! Here's how your content would look in Markdown format:

markdown
Copy code
## Useful Linux Commands and Deployment Steps Using AWS

### Installing Local Packages

To install a local package (.deb file) on Ubuntu using `dpkg`:

```bash
sudo dpkg -i app_file_name.deb
Make sure you're in the directory where app_file_name.deb is located.

Installing Git
To install Git on Ubuntu:

bash
Copy code
sudo apt install git
Removing Packages
To remove a package (wps-office as an example):
sudo apt-get remove wps-office
Replace pathToKey.pem with the path to your private key and publicIP with your instance's public IP.

Useful Linux Commands
Updating package lists and installing Python 3 pip:

bash
Copy code
sudo apt-get update && sudo apt-get install python3-pip
Installing Docker
Installing Docker on Ubuntu:

bash
Copy code
sudo apt install docker.io
Deploying HTML Website on EC2
Launch EC2 instance.
SSH into the instance.
Install Apache:
bash
Copy code
sudo apt install apache2
Place your HTML file in /var/www/html to serve it via the instance's public IP.
Deploying Application from GitHub to EC2
Generate SSH key on EC2:
bash
Copy code
ssh-keygen
Copy the public key (***.pub) to GitHub.
Clone the repository on EC2:
bash
Copy code
git clone repository_url
Install Python dependencies:
bash
Copy code
pip install -r requirements.txt
Run the application:
bash
Copy code
python3 application.py
Optionally use screen to keep the process running in the background.

Deploying Using Docker
Install Docker on EC2:
bash
Copy code
sudo apt install docker.io
Build Docker image from Dockerfile:
bash
Copy code
docker build -t imagename .
Run Docker container:
bash
Copy code
docker run -d -p 1122:8080 imagename
Access the application using http://ec2-public-ip:1122.

Installing MySQL on EC2
Install MySQL server on Ubuntu:

bash
Copy code
sudo apt install mysql-server
Start MySQL shell:

bash
Copy code
sudo mysql
Deployment Using CI/CD Pipeline
Launch Elastic Beanstalk (EBS) environment.
Configure CodePipeline with EBS and GitHub integration.
Set up .ebextensions/python.config.
Deploy your application.
Deployment Directly through EC2
Launch EC2 instance.
Generate SSH key pair.
Add the public key to GitHub.
Clone the GitHub repository on EC2 instance.
Install Python dependencies:
bash
Copy code
pip install -r requirements.txt
Run the Python application.
markdown
Copy code

### Common Linux Commands

- `gedit main.py`: Open a file in a text editor.
- `sudo apt-get update`: Update package lists.
- `sudo apt-get upgrade`: Upgrade installed packages.
- `sudo apt install snail`: Install software with root privileges.
- `sudo apt install vim`: Install Vim text editor.
- `sudo su`: Switch to root user.
- `sudo -i`: Switch to root user with environment variables.
- `man <command>`: View manual for a command.
- `pwd`, `ls`, `cd`, `mkdir`, `touch`, `rm`, `rmdir`: Basic file and directory operations.
- `head`, `tail`, `mv`, `cp`: View, move, and copy files.
- `chmod`: Change file permissions.
- `ps`, `top`, `htop`: View running processes.
- `kill <PID>`: Terminate a process.
- `vim <filename>`: Edit a file using Vim editor.
- `wget <url>`: Download a file from the internet.

These commands and steps are useful for setting up and managing applications, services, and environments on Linux systems, particularly on AWS EC2 instances.
