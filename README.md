![Jamulus banner](docs/assets/jamulusbannersmall.png)

# Jamulus server deployment with Ansible

Jamulus is for playing, rehearsing, or just jamming with your friends, your band or just anyone you find online.
You can join public servers or use this playbook to deploy a jamulus server in under 10 minutes
(or <30 minutes if you need to read up on basic server administration).

You will use your local computer to instruct a server how to install jamulus. You can also configure your server easily without much knowledge of server administration.


# Getting started

This playbook assumes you are operating on a linux system or [Windows Subsystem for Linux \(WSL\)](https://docs.microsoft.com/en-us/windows/wsl/about).

## Install ansible

Open a console and use the python package manager pip to install ansible to your local computer.

```bash
python3 -m pip install --user ansible
```

If you struggle with this step make sure pip is installed (`sudo apt install pip`) and check the [ansible documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

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


# TODO

* Make server publishable (change systemd jamulus command)