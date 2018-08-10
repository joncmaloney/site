---
layout: posts
title: Install Docker CE - CentOS
---


{{ page.title}}
==========================

source: https://docs.docker.com/install/linux/docker-ce/centos/

Install using the repository
-----------------------------
Before you install Docker CE for the first time on a new host machine, you need to set up the Docker repository. Afterward, you can install and update Docker

  ```bash
  $ sudo yum install -y yum-utils device-mapper-persistent-data lvm2
  ```



1. Install required packages. yum-utils provides the yum-config-manager utility, and device-mapper-persistent-data and lvm2 are required by the devicemappers

  ```bash
  $ sudo yum install -y yum-utils device-mapper-persistent-data lvm2
  ```

  

2. Use the following command to set up the stable repository. You always need the stable repository, even if you want to install builds from the edge or test

  ```bash
   $ sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
  ```

Install Docker CE
------------------
1. Install the latest version of Docker CE, or go to the next step to install a specific version

  ```bash
  $ sudo yum install docker-ce
  ```

  

2. Start docker daemon
   

  ```bash
  $ sudo systemctl start docker
  ```

  
