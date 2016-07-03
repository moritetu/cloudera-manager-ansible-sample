# Install Cloudera Manager with Ansible

This is a sample to install cloudera manager with ansible on vagrant virtual machines.

## Usage

1. Downloads mysql-connector-java and save it into `roles/cm/files`.
2. Runs vagrant and ansible playbook.

```
$ vagrant plugin install vagrant-hostmanager
$ vagrant up
$ ./vansible.sh playbook cdh.yml -vvv
```
