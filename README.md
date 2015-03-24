## [![Ansible project](http://vlead.virtual-labs.ac.in/VLEAD-small.png)](http://vlead.virtual-labs.ac.in)
# Nagios Ansible script for VLEAD

###O.S requirements:
Doing all the roles development and testing on CentOS machines for now.
Need to implement the same for ubuntu or debian based linux(future work)

###Description of roles:
There are two roles implemented in this repository
1. common.
2. common_vars.
3. nagios_server.
4. nagios_client.

# ansible-nagios
Ansible script to bringup a Nagios monitoring system and setup basic checks on hosts

Directory structure:
```
├── hosts
│   └── host_only(machines on which nagios server has to installed)
├── nagios_client.yml
├── nagios_server.yml(This script implements two roles common & nagios_server)
├── README.txt
└── roles
    ├── common
    │   ├── files
    │   │   └── history.sh
    │   ├── handlers
    │   │   └── main.yaml
    │   ├── meta
    │   │   └── main.yaml
    │   ├── tasks
    │   │   └── main.yaml
    │   ├── templates
    │   │   └── resolv.conf
    │   └── vars
    │       └── main.yaml
    ├── common_vars
    │   └── vars
    │       └── main.yml
    ├── nagios_client
    │   ├── defaults
    │   │   └── main.yml
    │   ├── handlers
    │   │   └── main.yml
    │   ├── tasks
    │   │   └── main.yml
    │   └── templates
    │       └── xinetd.conf.j2
    └── nagios_server
        ├── defaults
        │   └── main.yml
        ├── handlers
        │   └── main.yml
        ├── tasks
        │   ├── configure_servers.yml
        │   ├── configure_services.yml
        │   └── main.yml
        ├── templates
        │   ├── commands.cfg
        │   ├── configure_services.j2
        │   ├── contacts.cfg.j2
        │   ├── hostgroups.cfg
        │   ├── hosts.cfg
        │   └── services.cfg
        └── vars
            └── main.yml
    ```
