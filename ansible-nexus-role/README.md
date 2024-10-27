Repository: -git@github.com:debaj4life/ansible-nexus-role.git
Description:
The aim of this project to set up Nexus to store artifacts.
Prerequisites:

Ansible core version: ~>2.1.3
Python3: ~>3.1.2

Installation:

Install Python
Install Ansible core
Install Ansible Modules

Configuration: - Define the following

aws.ec2.yml
requirements.yml
site.yml
roles

Commands:

Install ansible role. Run the following command: ansible-galaxy install -r requirements.yml --roles-path roles

Deploy the Nexus Application. Run the following command: ansible-playbook -i aws_ec2.yml site.yml -b -u ec2-user --private-key=~/.ssh/file.pem


Accessing Nexus:

ssh into your server by running command - ssh -i "tutorial-key.pem" ec2-user@ec2-xx-xx-xxx-xx.eu-west-2.compute.amazonaws.com. Remember to amend ec2 ip address.
Enter https://nexus.tutorial.org into your browser.
Once you have successfully ssh into the server run command cat /opt/sonatype-work/nexus3/admin.password and copy the password.
Enter the credentials in nexus using;
username:admin
password: Paste password from previous step.
Then follow the instructions to reset the admin credentials to
username: admin
password: choose password.

Next steps:
For instructions on how to push jar files into nexus please click on the link here - https://lamtech.atlassian.net/wiki/spaces/DT/pages/1056112644/Upload+JAR+onto+NEXUS