# Apacke Jena + Fuseki

This repo is aimed to help spinning up VM with Jena + Fuseki installed. It runs fusekin on 3030 port with. Credentials:

* login: admin
* password: pw

Backups are available in host under `/fuseki/backups` folder.

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