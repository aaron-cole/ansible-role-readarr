# ansible-role-readarr

=========

Ansible Role to install readarr, an automated downloader, watchlist, monitoring program for ebooks.

Requirements
------------

Minimum Ansible version required is Ansible 2.9

Role Variables
--------------
Role variables have good defined defaults, which are located in `defaults/main.yml`.
Current version includes the following variables with default values:

### Defaults
| Name               | Default Value | Description                  |
|--------------------|---------------|------------------------------|
| `readarr_user`       | readarr | The primary user to run readarr  |
| `readarr_uid`        | *optional* | Commented out by default |
| `readarr_group`      | media | The primary group for `readarr_user` |
| `readarr_group_gid`  | *optional* | Commented out by default |
| `readarr_base_install_dir` | /opt | Base Install directory for readarr |
| `readarr_config_dir` |  /opt/data/readarr | Data directory to store configuration |
| `readarr_download_url` | https://readarr.servarr.com/v1/update/develop/updatefile?os=linux&runtime=netcore&arch=x64 | Link to the latest release |
| `readarr_port` | 8787 | Port in which readarr operates on, to add to Firewalld |
| `readarr_packages` |   ```- curl```  ```- sqlite``` | List of Packages Required to install and run readarr |

Dependencies
------------

None

Example Playbook
----------------

   - hosts: readarr_servers
      roles:
        - aaron-cole.ansible_role_readarr


License
-------

GPLv3

Author Information
------------------

Created by Aaron Cole


