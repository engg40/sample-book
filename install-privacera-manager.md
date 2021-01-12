# Install Privacera Manager

## Process Overview <a id="h2_1509357482"></a>

Privacera Manager provides a framework, process, installation components, configuration scripts, and property files for deploying, installing, and managing the deployment of all other Privacera components to target environments. Working within the Privacera Manager framework, you identify Privacera Platform components to be installed, configure those components by editing the properties files, and then invoking Privacera Manager. 

The general process for Privacera Manager is very similar for AWS and Azure,  but is adjusted for each.  The first step is to let Privacera Manager know the Cloud platform it is operating in. 

Privacera Manager itself is deployed using [Docker](https://docs.docker.com/) with [Docker Compose](https://docs.docker.com/compose/).  Once Privacera Manager is in place, it then runs and deploys Privacera Platform components either as Docker containers or within a Kubernetes cluster, so the second step is to select a preferred deployment.  The choice will depend on your deployment objectives,  target cloud platform and data repository types, and specific Privacera components.   After selecting your cloud platform, the second step is to select a deployment:

a\) Docker/Docker Compose will be the right choice for smaller 'single-node' configurations. A single-node, Docker deployed Privacera Platform uses fewer resources, but may not scale as well.

b\) A Kubernetes deployed Privacera Platform may use more resources but will scale, taking advantage of Kubernetes' ability to expand and add computation, memory, and storage resources, as needed. 

In addition to the 'core' functions:  Access Management, Discovery, and Encryption,  there are integration options for data repository systems, authentication integration options \(AD/LDAP\), optional SSO, security options, and audit logging options.   Privacera Manager provides individual configuration files to support each of these options. 

This document will help you select the method and the correct components for your environment. 

The rest of this user guide will provide specific installation steps.  The basic installation sequence is:

\(1\) Identify the target cloud platform;

\(2\) Select either a Docker or Kubernetes component deployment;

\(3\) Create a Privacera Manager 'host' virtual machine running your cloud environment with sufficient privileges to deploy and connect to the target data repositories.

     \(3a\) Configure the host system for Privacera Manager:  
             -  Install Docker & Docker Compose

\(4\) Download and install Privacera Manager;

\(5\) Run Privacera Manager to deploy and start core modules.

\(6\) After core modules are up and running, continue to configure additional modules and run Privacera Manager to update the deployment.  


     \(6a\) Locate matching configuration files and configure for your environment;

     \(6b\) Run Privacera Manager in 'update' mode.

## Whats Next - Create the Privacera Manager Host <a id="h2_1620375428"></a>

The next step is to create a Privacera Manager host system in your cloud environment.  This will be used to run Privacera Manager.  If a Docker/Docker Compose deployment is selected, it will also become the Privacera Platform host.  

If your cloud platform is AWS jump to the topic [Create Privacera Manager Host \(AWS\)](docker-installation-for-aws.html).

If your cloud platform is Azure, jump to topic [Create Privacera Manager Host \(Azure\)](docker-installation-for-azure.html).

 © Privacera, Inc. All rights reserved.  


