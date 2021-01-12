# \(Azure\) Create Privacera Manager Host

## What this does <a id="h2__1478472142"></a>

These are instructions for the creation of the Privacera Platform host in an Azure cloud environment.

The first step is to create a new virtual machine that will be dedicated to the Privacera Platform.  This virtual machine, along with your service account, must, initially, have sufficient privileges to allow it to download additional Privacera Platform required and optional components. Once running, this VM and associated service accounts, must also have sufficient privileges to the target data repositories and all other referenced resources. 

The second step is to install Docker and Docker Compose to the Privacera Manager host. 

|  |   Single-node/Docker deployment,  Privacera Manager deploys and configures Privacera Platform core components as assigned containers that run on the same platform.  In this 'single-node' configurations, the Privacera Manager host is also the Privacera Platform host. |
| :--- | :--- |


## Virtual Machine Creation <a id="h2_1084259820"></a>

Create an Azure Virtual Machine \(VM\) as follows:

* Ubuntu installed \(18.04.5 LTS preferable\)
* Open Ports

| **Port\(s\)** | **Service** |
| :--- | :--- |
| 6080  | Apache Ranger Admin  |
| 6182  | Apache Ranger Admin \(HTTPS\)  |
| 6868  | Privacera Portal  |
| 8181 \| 8282  | Privacera Dataserver \(Endpoint\)  |
| 9191  | Privacera Dataserver \(Proxy\)  |
| 8983  | Apache Solr  |
| 2181  | Apache Zookeeper  |
| 22  | SSH  |
| \* | Self Security Group  |

## Install Docker and Docker Compose <a id="h2__2051240644"></a>

1. SSH to the VM as the administrator \( ${VM\_USER} \).
2. Install Docker on the VM.

   | Bash \(Unix Shell\) |
   | :--- |
   |  |

3. Reattach to the VM \(SSH to VM as ${VM\_USER}\).
4. Confirm docker installation Download Docker-compose.

   | Bash \(Unix Shell\) |
   | :--- |
   |  |

### What's Next: <a id="h3_1518538595"></a>

### [**Configure and Install Core Services**](bootstrap-privacera-manager.html)  <a id="h3_816878452"></a>

 © Privacera, Inc. All rights reserved.  


