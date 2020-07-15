# Ansible-Sample-Application-Deployment
This repository will contain sample code to deploy the sample application on linux instance

# Directory Structure
  - configs - contain environment specific variable
  - inventories - contains inventory file for each environment
  - groups_vars - contains common variables across environments
  - roles - This will have subfolders as per need java,tomcat
       - tomcat - this folder will files related to the installation of tomcat
       
              - files (This will contain files which you want to copy to to your destination servers)

              - handlers ( This is used to start/stop the services)

              - templates (This will contain template files)

              - tasks ( playbook to install the software)

  - main.yml - This is the main file which will execute roles in the playbook

s