# ansible-nagios
Ansible script to bringup a Nagios monitoring system and setup basic checks on hosts

Directory structure:
.
├── hosts
│   └── host_only
├── nagios_client.yml
├── nagios_server.yml
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
