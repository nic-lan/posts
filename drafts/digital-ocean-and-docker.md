# Digital Ocean and Docker

How to set use docker and docker machine with digital ocean and deploy a service 

## A short introduction

Recently I started to get interested into [Docker](https://www.docker.com/), the software container platform. 

Now after a few months i decided that it could have been funny to use docker again in order to deploy my personal web site [niclan.io](niclan.io) in order to take full control of the stack from setting up the machine till the deploy and the hosting of the service.

In order to do that i decided to go for [Digital Ocean](https://www.digitalocean.com/) because it provides some support for docker and docker-machine. 

A valid alternative to digital ocean that I already had the chance to try are [Amazon AWS](https://aws.amazon.com/it/) and in particular its [EC2](https://aws.amazon.com/it/ecs/) container service.
  
 So here below the process i followed:
 
 ## Requirements
 
 You need to sign up with digital ocean and to have docker and docker machine installed.
 
 ## Setting up the droplet
 
 Basically the main resource I used to set up the droplet and the container is this [article](https://docs.docker.com/machine/examples/ocean/#step-4-run-docker-commands-on-the-droplet).
 
 After signing up and getting my personal token I created my very first droplet.
 
```
$ docker-machine create --driver digitalocean --digitalocean-access-token xxxxx docker-sandbox nic-lan-web
Running pre-create checks...
Creating machine...
(nic-lan-web) OUT | Creating SSH key...
(nic-lan-web) OUT | Creating Digital Ocean droplet...
(nic-lan-web) OUT | Waiting for IP address to be assigned to the Droplet...
Waiting for machine to be running, this may take a few minutes...
Machine is running, waiting for SSH to be available...
Detecting operating system of created instance...
Detecting the provisioner...
Provisioning created instance...
Copying certs to the local machine directory...
Copying certs to the remote machine...
Setting Docker configuration on the remote daemon...
To see how to connect Docker to this machine, run: docker-machine env nic-lan-web
```
 
