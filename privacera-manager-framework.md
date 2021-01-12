# Privacera Manager Framework

Privacera Manager functions as a framework of shell and Ansible scripts, and configuration files. 

The Privacera Manager compressed wrapper unpacks to  the following directory structure:

├── ansible

│   ├── privacera-docker

│   └── run\_playbook.sh

├── config

│   ├── custom-properties

│   ├── custom-vars

│   ├── sample-vars

│   ├── sample.ansible.cfg

│   ├── sample.pm-env.sh

│   ├── sample.privacera.inventory

│   └── sample.vars.privacera.yml

├── privacera-manager.sh

├── privacera\_version.txt

├── scripts

│   └── privacera-ctl.sh

└── setup\_privacera.sh

The default installation is to  "~/privacera/privacera-manager" \(a subfolder of the installer's home folder\).  


 There is a single top-level script,  "**privacera-manager.sh"**, which drives all the other subscripts.  It locates the custom variable configuration files, invokes the appropriate Ansible scripts as needed, and initiates those scripts to install the configured Privacera components. This shell script must be executed each time there is a set of custom property files created or modified. 

Once the initial Privacera Manager download is complete, the setup process for each component is identical:

1. Locate a template properties file in 'config/sample-vars/' and copy it to 'config/custom-vars/'.  
2. Edit the new property file \(in config/custom-vars/\) for your requirements and site. 

These steps can be repeated multiple times, once for each unique Privacera component. 

When the configuration of the selected components is complete run "./privacera-manager.sh update".

 © Privacera, Inc. All rights reserved.  


