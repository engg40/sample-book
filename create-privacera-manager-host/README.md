# Create Privacera Manager Host

The first step is to create a new virtual machine that will be dedicated to the Privacera Platform.  This virtual machine, along with your service account, must, initially, have sufficient privileges to allow it to download additional Privacera Platform required and optional components.   
  
Once running, this VM and associated service accounts, must also have sufficient privileges to the target data repositories and all other referenced resources. 

The second step is to install Docker and Docker Compose to the Privacera Manager host. 

| ![Information](https://docs2.privacera.com/resources/Storage/ex-privacera-manager/info.png) |   Single-node/Docker deployment,  Privacera Manager deploys, and configures Privacera Platform core components as Docker containers that run on this same virtual machine.  In this 'single-node' configurations, the Privacera Manager host is also the Privacera Platform host. |
| :--- | :--- |


