# \(AWS\) Create Privacera Manager Host

## What this does <a id="h2__771625279"></a>

These are instructions for the creation of the Privacera Platform host in an AWS cloud environment.

The first step is to create a new virtual machine that will be dedicated to the Privacera Platform.  This virtual machine, along with your service account, must, initially, have sufficient privileges to allow it to download additional Privacera Platform required and optional components. Once running, this VM and associated service accounts, must also have sufficient privileges to the target data repositories and all other referenced resources. 

The second step is to install Docker and Docker Compose to the Privacera Manager host. 

|  |   Single-node/Docker deployment,  Privacera Manager deploys, and configures Privacera Platform core components as Docker containers that run on this same virtual machine.  In this 'single-node' configurations, the Privacera Manager host is also the Privacera Platform host. |
| :--- | :--- |


## Virtual Machine Creation <a id="h2_271279321"></a>

### Create an AWS EC2 Instance <a id="h3_836460192"></a>

Configured as follows:

*  **AMI:**                   Amazon Linux AMI 6-bit x86 SSD 
*  **Instance Type:**  m5.2xlarge or larger
* **Storage:**            Primary \(Root\) volume \(/dev/xvda\) minimum size 128 GiB,  General Purpose SSD \(gp2\)
*  **Tags:**                  As useful for your organization.
* **Role:**                  Create a new IAM Role. Give this IAM role 'AdministrativeAccess'.  Name it "Privacera\_PM\_Role" \(This can be done in the Instance creation wizard sequence\) 
*  **Network & VPC** with attached **Security Group**  with ports ingress/egress set as follows:

 **Inbound Ports \(TCP\):**   

6080               \(Apache Ranger Admin\)

6182               \(Apache Ranger Admin \(HTTPS\)\)

6868               \(Privacera Portal\)

8181 / 8282    \(Privacera Dataserver \(Endpoint\)\)

9191                \(Privacera Dataserver \(Proxy\)\)

8983                \(Apache Solr\)

2181                \(Apache Zookeeper\) 

22                    \(SSH\) 

\*                      Self Security Group  


 **Outbound Ports \(TCP\):**

80 \(for initial setup and download\)

## Install Docker and Docker Compose <a id="h2__1478472142"></a>

Docker is used by Privacera Manager.

1.  Log on to your Privacera host as ec2-user or a user with 'sudo' privileges.
2. Install Docker:  
   \(a\) Use 'yum' to obtain Docker;  
   \(b\) Reconfigure limits;  
   \(c\) Start Docker Service  
   \(d\) Add your root user \(e.g. 'ec2-user'\) to the docker group.  
   \(e\) Exit

   From the command prompt execute the following:

   | Bash \(Unix Shell\) |
   | :--- |
   |  |

3. Log back into the same user account as in step 1. \(This forces the **usermod** action\). 
4. Install Docker-Compose:
   1.  Set the requested Docker Compose version;  
   2.  Download  docker-compose
   3.  Set access to eXecutable

      | Bash \(Unix Shell\) |
      | :--- |
      |  |

### What's Next: <a id="h3_1518538595"></a>

[**Configure and Install Core Services**](bootstrap-privacera-manager.html)  


 © Privacera, Inc. All rights reserved.  


