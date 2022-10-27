# Monitoring via Ansible


This playbook helps you to deploy a jamulus server in under 10 minutes
(or an hour if you need to read up on basic server administration).


# Getting started

This playbook assuems you are operating on a linux system with ansible already installed.

## Configure

Follow the steps in [Configuration](docs/configuring-playbook.md)

## Install the server

Install everything with

```shell
ansible-playbook -i inventory/hosts setup.yml --tags=all
```

## Restore

When you somehow lost your vars file (that is not under version control) you can find it under `/jamulus/vars.yml`. on the server.
You can deactivate this behaviour by setting `vars_yml_snapshotting_enabled: false`