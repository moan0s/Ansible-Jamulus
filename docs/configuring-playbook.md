# Configuring the Ansible playbook

To configure the playbook, you need to have done the following things:

- have a ubuntu or debian server where jamulus will run. Hetzners CX11 is a very reliable and reasonably cheap (<5€/month) server and set up in minutes. Use [this link]([Hetzner](https://hetzner.cloud/?ref=B77yGmfF39CQ)) to have a credit of 20€ (affiliate link).
- [configured your DNS records](configuring-dns.md)
- [retrieved the playbook's source code](getting-the-playbook.md) to your computer

You can then follow these steps inside the playbook directory:

1. create a directory to hold your configuration (`mkdir inventory/host_vars/matrix.<your-domain>`)
2. copy the sample configuration file (`cp examples/vars.yml inventory/host_vars/matrix.<your-domain>/vars.yml`)
3. edit the configuration file (`inventory/host_vars/matrix.<your-domain>/vars.yml`) to your liking. You may also take a look at the various `roles/ROLE_NAME_HERE/defaults/main.yml` files and see if there's something you'd like to copy over and override in your `vars.yml` configuration file.
4. copy the sample inventory hosts file (`cp examples/hosts inventory/hosts`)
5. edit the inventory hosts file (`inventory/hosts`) to your liking


For a basic Matrix installation, that's all you need.