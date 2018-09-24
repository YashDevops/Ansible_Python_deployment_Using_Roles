# Ansible_Python_deployment_Using_Roles

## This is modular feature of to deploy python application using roles. 
## To use this just perform the following task
```shell

Vagrant up


### This will create 4 box naming app01 , app02 , lb01 , db01


## lb01 (Load balancer)


## db01 (DataBase Server)


## app01 and app02 (Webserver)



To run it use the following command
```shell

ansible-playbook sites.yml -u vagrant -k 

```

## After you have launched your configuration you can use the stack_restart at any time to restart the complete stack

```shell

ansible-playbook stack_restart.yml -u vagrant -k

``` 

The app server configuration is done by using apache2 and the following tasks are achieve using ansible
### 1) The apt install are done using {{item}} loops and 
### 2) Thec complete app is copied using ansible copy module
### 3) The virtual environment is created using pip module 
### 4) All the configuration changes are done using file module
