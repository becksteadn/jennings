Role Name
=========

This role installs an Apfell payload as a script in a `rc` directory.

Requirements
------------

* An [Apfell](https://github.com/its-a-feature/Apfell) server
* A compiled payload file in the `files` directory or link to the hosted file.

Role Variables
--------------

```
payload_type (viper) - Type of payload (viper, linfell, apfell-jxa)
required_packages (python-minimal) - System packages that need to be installed for the payload to run. (Python2.7 for viper payloads)
filename (viper.py) - Local payload filename
copy_file (True) - Copy the payload from local machine to remote machine
download_file (False) - Download the payload from a URL
download_base_url (http://example.com:80/) - URL and directory path for payload. Followed by 'filename'.
remote_file_location (/usr/lib/viper) - Full path to place payload
service_filename (plant.service) - Local filename to copy for runlevel script
service_name (viper) - Name of service to link in rc directory
run_dir (/tmp/) - Directory to start process in
run_cmd (/usr/bin/python) - Command to start process. Followed by 'remote_file_location'.
run_user (root) - User to run process as
init_run_level (2) - Run level to run as 
init_run_prefix (S01) - File prefix for rc file
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      become: yes
      roles:
         - plant

License
-------

BSD

Author Information
------------------

github.com/becksteadn
