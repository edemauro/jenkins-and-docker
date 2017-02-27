This project was set up to familiarize myself with Jenkins. 

The Jenkins master server is hosted in a Docker container.

Vagrant along with Ansible is used to create a docker host in a virtual machine that spins up build slaves.

## Installation

1. Use Docker Compose to create the Jenkins master with a data container.

```bash
$ docker-compose build
```

2. Create the docker host with Vagrant and Ansible.

```bash
$ vagrant up
```

3. Install the following plugins:
jCloud plugin
Docker plugin

4. Add the dummy RSA private key as global credentials.

5. Configure Jenkins to communicate with the docker host using the following settings:
Docker URL: tcp://192.168.10.10:2375
Docker Image: jenkins-slave
Remote Filing System Root: /home/jenkins
Remote FS Root Mapping: /home/jenkins
Credentials: The credentials added in step #4