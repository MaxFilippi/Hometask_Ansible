# LAMP on Ubuntu 18.04

This role will install a LAMP environment (**L**inux, **A**pache, **M**ySQL and **P**HP) on an Ubuntu 18.04 machine, as explained in the guide on [How to Use Ansible to Install and Configure LAMP on Ubuntu 18.04](#). A virtualhost will be created with the options specified in the `vars/default.yml` variable file.

## Settings

- `mysql_root_password`: the password for the MySQL root account.
- `app_user`: a remote non-root user on the Ansible host that will own the application files.
- `http_host`: your domain name.
- `http_conf`: the name of the configuration file that will be created within Apache.
- `http_port`: HTTP port, default is 80.
- `disable_default`: whether or not to disable the default Apache website. When set to true, your new virtualhost should be used as default website. Default is true.



### Customize Options

```shell
nano vars/default.yml
```

```yml
---
mysql_root_password: "testadmin"
app_user: "fill"
http_host: "ans-node01"
http_conf: "ans-node01.conf"
http_port: "80"
disable_default: true
```
