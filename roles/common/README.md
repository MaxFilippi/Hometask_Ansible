# Initial Server Setup on Ubuntu 18.04

This role will execute a initial server setup for Ubuntu 18.04 systems, as explained in the guide on
[Initial Server Setup Guide for Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-automate-initial-server-setup-on-ubuntu-18-04).
A number of containers will be created with the options specified in the `vars/default.yml` variable file.

## Settings

- `create_user`: the name of the remote sudo user to create.
- `copy_local_key`: path to a local SSH public key that will be copied as authorized key for the new user. By default, it copies the key from the current system user running Ansible.
- `sys_packages`: array with list of packages that should be installed.


###  Customize Options

```shell
vars/main.yml
```

