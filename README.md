# Ansible-Sample-Application-Deployment
This repository will contain sample code to deploy the sample application on linux instance




# Directory Structure
  1. configs - contain environment specific variable
  2. inventories - contains inventory file for each environment
  3. groups_vars - contains common variables across environments
  4. roles - This will have subfolders like java,tomcat

       a) tomcat - this folder will have files related to the installation of tomcat

              - files (This will contain files which you want to copy to to your destination servers)

              - handlers ( This is used to start/stop the services)

              - templates (This will contain template files)

              - tasks ( playbook to install the software)

        b) java - This folder will have files related to the installation of java

  5. main.yml - This is the main file which will execute roles in the playbook


# How to Run the Playbook

https://stackabuse.com/how-to-fix-warning-unprotected-private-key-file-on-mac-and-linux/

```
ansible-playbook main.yml -i inventories/dev/hosts ---user ec2-user
--key-file /home/ec2-user/playbooks/ansible_auto.pem

ansible-playbook main.yml -i inventories/dev/hosts - e configs/dev.yaml


```
# References


