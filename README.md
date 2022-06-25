## Introduction
For GIT (Github) testing only! Ansible playbooks for fast services configuration
## Current Releases
0.1 - Initial Commit <br />
0.2 - Same playbook for CentOS 9
## Platforms
Tested in Debian 11.3 netinst and CentOS 9 Stream. Required sudo installed and user must be in the sudo (wheel for CentOS) group. <br />
## Usage
Typical usage:
```
ansible-playbook -i autoweb.yml --ask-pass
```
See more using notices in playbooks. <br />
Do not forget to change your server url, user logins and database name before start. <br />
You can grab admin and user passwords from *connect.php* file in server's root folder after installation. <br />
If you accidentally deleted *connect.php* file and forgot to copy from terminal, you can restart playbook, this action will regenerate passwords for you. <br />
Debian 11.3 has *php 7.4* in repos. You may need to modify php-fpm version in *domain.local.j2* config file: *fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;*. <br />
## Licenses
Use and modify on your own risk.