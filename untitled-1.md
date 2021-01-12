# Introduction

## Privacera Manager <a id="h2_1509357482"></a>

Privacera Manager \("**PM**"\) is an installation framework for installing and updating Privacera Platform components.  

## Privacera Platform <a id="h2_1136017954"></a>

Privacera provides:

* **Access Management**         Data access monitoring and policy-based control for data governance;
* **Data Discovery**:                 Find, classify, and tag sensitive data;
* **Encryption and Masking**:   Encryption and mask, and 'anonymization' of sensitive data; 

### Access Management Integration <a id="h3_223377605"></a>

There are three primary methods of integration. These are:

* **Plug-In:**     Data repository systems, such as Databricks Spark, EMR PrestoDB, and EMR Hive have integrated as a 'plug-in' control support for external authentication.  This is the most direct and efficient method and is entirely transparent to the data users. 
* **Data-Access \(Proxy\) Server**:   In this method, data access requests are re-directed to a Privacera authentication broker' proxy inserted into the control and data flow   Control flow is redirected to the authentication broker, and actual authentication methods proceed as with the Plug-in approach.  The Privacera authentication broker may be used with external authentication or directory service such as  MS Active Directory, SAML, OpenID, OAuth, and Kerberos.
* **Policy Sync**:  In this method, access policies defined in Privacera are mapped to and 'synchronized' to the 'native' access controls available in the target data repository.  This approach is used where data is accessed 'natively', MS SQL, AWS Redshift, etc.

 © Privacera, Inc. All rights reserved.  


