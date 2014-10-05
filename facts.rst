=====
Facts
=====


Example facts generated from a Vagrant instance::

  {
    "ansible_facts": {
        "ansible_all_ipv4_addresses": [
            "10.0.2.15"
        ],
        "ansible_all_ipv6_addresses": [
            "fe80::a00:27ff:fe88:ca6"
        ],
        "ansible_architecture": "x86_64",
        "ansible_bios_date": "12/01/2006",
        "ansible_bios_version": "VirtualBox",
        "ansible_cmdline": {
            "BOOT_IMAGE": "/vmlinuz-3.2.0-58-generic",
            "quiet": true,
            "ro": true,
            "root": "/dev/mapper/precise64-root"
        },
        "ansible_date_time": {
            "date": "2014-02-10",
            "day": "10",
            "epoch": "1392003568",
            "hour": "03",
            "iso8601": "2014-02-10T03:39:28Z",
            "iso8601_micro": "2014-02-10T03:39:28.048618Z",
            "minute": "39",
            "month": "02",
            "second": "28",
            "time": "03:39:28",
            "tz": "UTC",
            "tz_offset": "+0000",
            "year": "2014"
        },
        "ansible_default_ipv4": {
            "address": "10.0.2.15",
            "alias": "eth0",
            "gateway": "10.0.2.2",
            "interface": "eth0",
            "macaddress": "08:00:27:88:0c:a6",
            "mtu": 1500,
            "netmask": "255.255.255.0",
            "network": "10.0.2.0",
            "type": "ether"
        },
        "ansible_default_ipv6": {},
        "ansible_devices": {
            "sda": {
                "holders": [],
                "host": "SATA controller: Intel Corporation 82801HM/HEM (ICH8M/ICH8M-E) SATA Controller [AHCI mode] (rev 02)",
                "model": "VBOX HARDDISK",
                "partitions": {
                    "sda1": {
                        "sectors": "497664",
                        "sectorsize": 512,
                        "size": "243.00 MB",
                        "start": "2048"
                    },
                    "sda2": {
                        "sectors": "2",
                        "sectorsize": 512,
                        "size": "1.00 KB",
                        "start": "501758"
                    },
                    "sda5": {
                        "sectors": "167268352",
                        "sectorsize": 512,
                        "size": "79.76 GB",
                        "start": "501760"
                    }
                },
                "removable": "0",
                "rotational": "1",
                "scheduler_mode": "cfq",
                "sectors": "167772160",
                "sectorsize": "512",
                "size": "80.00 GB",
                "support_discard": "0",
                "vendor": "ATA"
            },
            "sr0": {
                "holders": [],
                "host": "IDE interface: Intel Corporation 82371AB/EB/MB PIIX4 IDE (rev 01)",
                "model": "CD-ROM",
                "partitions": {},
                "removable": "1",
                "rotational": "1",
                "scheduler_mode": "cfq",
                "sectors": "2097151",
                "sectorsize": "512",
                "size": "1024.00 MB",
                "support_discard": "0",
                "vendor": "VBOX"
            },
            "sr1": {
                "holders": [],
                "host": "IDE interface: Intel Corporation 82371AB/EB/MB PIIX4 IDE (rev 01)",
                "model": "CD-ROM",
                "partitions": {},
                "removable": "1",
                "rotational": "1",
                "scheduler_mode": "cfq",
                "sectors": "2097151",
                "sectorsize": "512",
                "size": "1024.00 MB",
                "support_discard": "0",
                "vendor": "VBOX"
            }
        },
        "ansible_distribution": "Ubuntu",
        "ansible_distribution_release": "precise",
        "ansible_distribution_version": "12.04",
        "ansible_domain": "",
        "ansible_env": {
            "HOME": "/home/vagrant",
            "LANG": "C",
            "LC_ALL": "en_US",
            "LC_CTYPE": "en_US.UTF-8",
            "LOGNAME": "vagrant",
            "MAIL": "/var/mail/vagrant",
            "PATH": "/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games",
            "PWD": "/home/vagrant",
            "SHELL": "/bin/bash",
            "SHLVL": "1",
            "SSH_AUTH_SOCK": "/tmp/ssh-ckWMnB5666/agent.5666",
            "SSH_CLIENT": "10.0.2.2 59664 22",
            "SSH_CONNECTION": "10.0.2.2 59664 10.0.2.15 22",
            "SSH_TTY": "/dev/pts/1",
            "TERM": "xterm",
            "USER": "vagrant",
            "_": "/bin/sh"
        },
        "ansible_eth0": {
            "active": true,
            "device": "eth0",
            "ipv4": {
                "address": "10.0.2.15",
                "netmask": "255.255.255.0",
                "network": "10.0.2.0"
            },
            "ipv4_secondaries": [],
            "ipv6": [
                {
                    "address": "fe80::a00:27ff:fe88:ca6",
                    "prefix": "64",
                    "scope": "link"
                }
            ],
            "macaddress": "08:00:27:88:0c:a6",
            "module": "e1000",
            "mtu": 1500,
            "promisc": false,
            "type": "ether"
        },
        "ansible_form_factor": "Other",
        "ansible_fqdn": "precise64",
        "ansible_hostname": "precise64",
        "ansible_interfaces": [
            "lo",
            "eth0"
        ],
        "ansible_kernel": "3.2.0-58-generic",
        "ansible_lo": {
            "active": true,
            "device": "lo",
            "ipv4": {
                "address": "127.0.0.1",
                "netmask": "255.0.0.0",
                "network": "127.0.0.0"
            },
            "ipv4_secondaries": [],
            "ipv6": [
                {
                    "address": "::1",
                    "prefix": "128",
                    "scope": "host"
                }
            ],
            "mtu": 16436,
            "promisc": false,
            "type": "loopback"
        },
        "ansible_lsb": {
            "codename": "precise",
            "description": "Ubuntu 12.04.4 LTS",
            "id": "Ubuntu",
            "major_release": "12",
            "release": "12.04"
        },
        "ansible_machine": "x86_64",
        "ansible_memfree_mb": 41,
        "ansible_memtotal_mb": 365,
        "ansible_mounts": [
            {
                "device": "/dev/mapper/precise64-root",
                "fstype": "ext4",
                "mount": "/",
                "options": "rw,errors=remount-ro",
                "size_available": 77439922176,
                "size_total": 83500965888
            },
            {
                "device": "/dev/sda1",
                "fstype": "ext2",
                "mount": "/boot",
                "options": "rw",
                "size_available": 174159872,
                "size_total": 238787584
            }
        ],
        "ansible_os_family": "Debian",
        "ansible_pkg_mgr": "apt",
        "ansible_processor": [
            "Intel(R) Core(TM) i7-4960HQ CPU @ 2.60GHz",
            "Intel(R) Core(TM) i7-4960HQ CPU @ 2.60GHz"
        ],
        "ansible_processor_cores": 2,
        "ansible_processor_count": 1,
        "ansible_processor_threads_per_core": 1,
        "ansible_processor_vcpus": 2,
        "ansible_product_name": "VirtualBox",
        "ansible_product_serial": "NA",
        "ansible_product_uuid": "NA",
        "ansible_product_version": "1.2",
        "ansible_python_version": "2.7.3",
        "ansible_selinux": false,
        "ansible_ssh_host_key_dsa_public": "AAAAB3NzaC1kc3MAAACBAJwR6q4VerUDe7bLXRL6ZPTXj5FY66he+WWlRSoQppwDLqrTG73Pa9qUHMDFb1LXN1qgg0p0lyfqvm8ZeN+98rbT0JW6+Wqa7v0K+N82xf87fVkJcXAuU/A8OGR9eVMZmWsIOpabZexd5CHYgLO3k4YpPSdxc6S4zJcOGwXVnmGHAAAAFQDHjsPg0rmkbquTJRdlEZBVJe9+3QAAAIBjYIAiGvKhmJfzDjVfzlxRD1ET7ZhSoMDxU0KadwXQP1uBdlYVEteJQpUTEsA+7kFH7xhtZ/zbK2afEFHriAphTJmz8GqkIR5CJXh3dZspdk2MHCgxkXl5G/iVPLR9UShN+nsAVxfm0gffCqbqZu3Ridt3JwTXQbiDfXO/a6T/eQAAAIEAlsW/i/dUuFbRVO2zaAKwL/CFWT19Al7+njszC5FCJ2deggmF/NIKJUbJwkRZkwL4PY1HYj2xqn7ImhPSyvdCd+IFdw73Pndnjv0luDc8i/a4JUEfna4rzXt1Y5c24J1pEoKA05VicyCBD2z6TodRJEVEFSsa1s8s2p9x6LxwsDw=",
        "ansible_ssh_host_key_ecdsa_public": "AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBFxsiWE3WImfJcjiWS5asOVoMsn+0gFLU5AgPNs2ATokB7kw00IsB0YGrqClwYNauRRddkYMsi0icJSR60mYNSo=",
        "ansible_ssh_host_key_rsa_public": "AAAAB3NzaC1yc2EAAAADAQABAAABAQDZt46W9slSN3Y6D2f931rijUPCEewhQWmBfGhybuF4qLftfJMuyFcREZkG6UretVI8ZnQn/OMDgbf2DYMzKsRLnz7W5cGy1Mt1pWoG0iCgi2xHzLqOqPYo4mP9/hdZT6pANXapETT55yx8sHAYLAa9NK5Dtyv+QNQ2dUUb1wUTCqgYffLVDgoHvNNDwCwB6biJf6uopqfg2KXvAzcqSa6oaRChJOXjFlM08HebMwkMSzrOXjWbXhFsONy5JuDf3WztCtLMsFrVRHTdDwTh7uL2UQ8Qcky+kP6Wd7G8NlW5RxubYIFpAM0u2SsQIjYOxz+eOfQ8GE3WjvaIBqX05gat",
        "ansible_swapfree_mb": 767,
        "ansible_swaptotal_mb": 767,
        "ansible_system": "Linux",
        "ansible_system_vendor": "innotek GmbH",
        "ansible_user_id": "vagrant",
        "ansible_userspace_architecture": "x86_64",
        "ansible_userspace_bits": "64",
        "ansible_virtualization_role": "guest",
        "ansible_virtualization_type": "virtualbox"
    }
