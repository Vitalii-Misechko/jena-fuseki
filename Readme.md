# Vagrant files for Apache Jena + Fuseki

This repo is aimed to help spinning up VM with Jena + Fuseki installed on local computer. It runs fuseki on 3030 port. 
Credentials:

* login: admin
* password: pw

Backups are available in the host VM under `/fuseki/backups` folder.

## Installation

You need to install:

1. Virtualbox
2. Vagrant
3. Execute the following command from the project directory:
```
vagrant up
```
You might see an error like below. Ignore it
```
Stderr: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock
```
4. Execute following command once again
```
vagrant up
```

## Clean up

1. Execute
```
vagrant destroy
```
2. Execute 
```
vagrant global-status
```
Follow output instructions