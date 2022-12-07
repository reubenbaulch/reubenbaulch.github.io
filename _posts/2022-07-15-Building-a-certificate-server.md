---
title: "Building a certificate server"
layout: post
---

In this project, I built a certificate server using server manager on a domain controller. 

### Technologies Used: 
 
* Active directory
* Windows server manager

### Building the certificate server

Firstly, I added roles and features, using a role based/feature based installation on a running virtual machine. Next, I installed active directory certificate services on the selected server with the .NET framework 4.7 feature. This included configuring the active directory certificate service and specifying the credentials to configure the role services (certificate authority). I selected an enterprise CA as a root CA (top of the PKI hierarchy).
Following this, I generated a new private key for the CA to issue certificates to the clients using RSA with a key length of 2048. I used SHA256 as the hash algorithm for signing the certificate that would be issued by the CA. I finished off by setting the name and validity period for the certificate as well as the database location.

![title](/pics/certificate-server/ADCSConfiguration.png)

### Encrypting data with EFS and stealing certificates

Using windows encrypting content feature, I encrypted test data with EFS. I then used Microsoft's management console to add a snap-in certificate under the current user. Next, I exported the certificate using the certificate export wizard in p12 format.

![title](/WindowsServerMonitoring.png)

After confirming the password, I selected tripleDES-SHA1 for encryption and exported the certificate. I then followed the same steps for exporting the public key.

![title](/WindowsServerMonitoring.png)

### Revoking the EFS certificate

Finally, I revoked the issued certificates using server manager due to key compromise (the certificates private key was exposed)
