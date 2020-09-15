---
title: Installing Red Hat(Code Ready Containers) on Ubuntu 20.04
date: "2015-05-01T22:12:03.284Z"
description: "Lets get going with code Ready contianer installed on Ubuntu 20.04"
---


#Pre-requisits:

Install `libvirt` and `NetworkManager` packages for ubuntu 


- This can be achieved by running the following command:

```
sudo apt install qemu-kvm libvirt-daemon libvirt-daemon-system network-manager)=

```



- install Docker.io for ubuntu This can be achieved by running the following commands:

```

 sudo apt install docker.io
 sudo apt-get remove docker docker-engine docker.io

 sudo apt install docker.io

 sudo systemctl start docker

 sudo systemctl enable docker

```
- Step 1. Login to cloud.redhat.com at the time of writing this article its on 

Choice `create cluster` - Openshift Container Platform 4- Run on local laptop option.

Download the CRC for Linux in this case because we are on Ubuntu.


 Download the CDK from cloud.redhat.com at the time of writing this article its on `OpenShift 4.3.10`

- Step 2. https://cloud.redhat.com/openshift/install/crc/installer-provisioned


Once you have the crc downloaded extract the files and place your binary shells path 
```

e.g '/usr/bin/'.

````

- Step 3. Once install run the following

```
anyte25@nanyte25-NUC8i7BEH:~/Documents/markfreer$ crc setup
INFO Checking if oc binary is cached              
INFO Checking if podman remote binary is cached   
INFO Checking if CRC bundle is cached in '$HOME/.crc' 
INFO Checking if running as non-root              
INFO Checking if Virtualization is enabled        
INFO Checking if KVM is enabled                   
INFO Checking if libvirt is installed             
INFO Checking if user is part of libvirt group    
WARN Skipping above check ...                     
INFO Checking if libvirt is enabled               
INFO Checking if libvirt daemon is running        
INFO Checking if a supported libvirt version is installed 
INFO Checking if crc-driver-libvirt is installed  
INFO Checking for obsolete crc-driver-libvirt     
INFO Checking if libvirt 'crc' network is available 
INFO Checking if libvirt 'crc' network is active  
INFO Checking if NetworkManager is installed      
WARN Skipping above check ...                     
INFO Checking if NetworkManager service is running 
WARN Skipping above check ...                     
INFO Checking if /etc/NetworkManager/conf.d/crc-nm-dnsmasq.conf exists 
WARN Skipping above check ...                     
INFO Checking if /etc/NetworkManager/dnsmasq.d/crc.conf exists 
WARN Skipping above check ...                     
Setup is complete, you can now run 'crc start' to start the OpenShift cluster


```
- Step 4. Run `crc start` and login with your `Red Hat` developer account.

```

 crc start
WARN A new version (1.16.0) has been published on https://cloud.redhat.com/openshift/install/crc/installer-provisioned 
INFO Checking if oc binary is cached              
INFO Checking if podman remote binary is cached   
INFO Checking if running as non-root              
INFO Checking if Virtualization is enabled        
INFO Checking if KVM is enabled                   
INFO Checking if libvirt is installed             
INFO Checking if user is part of libvirt group    
WARN Skipping above check ...                     
INFO Checking if libvirt is enabled               
INFO Checking if libvirt daemon is running        
INFO Checking if a supported libvirt version is installed 
INFO Checking if crc-driver-libvirt is installed  
INFO Checking if libvirt 'crc' network is available 
INFO Checking if libvirt 'crc' network is active  
INFO Checking if NetworkManager is installed      
WARN Skipping above check ...                     
INFO Checking if NetworkManager service is running 
WARN Skipping above check ...                     
INFO Checking if /etc/NetworkManager/conf.d/crc-nm-dnsmasq.conf exists 
WARN Skipping above check ...                     
INFO Checking if /etc/NetworkManager/dnsmasq.d/crc.conf exists 
WARN Skipping above check ...                     
INFO Starting CodeReady Containers VM for OpenShift 4.3.10... 
INFO Verifying validity of the cluster certificates ... 
INFO Check internal and public DNS query ...      
INFO Check DNS query from host ...                
INFO Cluster TLS certificates have expired, renewing them... [will take up to 5 minutes] 

```