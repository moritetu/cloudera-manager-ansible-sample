# Install Cloudera Manager with Ansible

This is a sample to install cloudera manager with ansible on vagrant virtual machines.

## Usage

Download mysql-connector-java.


Run vagrant and ansible playbook.

```
$ vagrant plugin install vagrant-hostmanager
$ vagrant up
$ ./vansible.sh playbook cdh.yml -vvv
```
