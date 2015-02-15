=====
Facts
=====

Example facts generated from a Vagrant machine.

Facts that start with ``facter_``
will only be collected if the facter_ program is present. Facts that start with
``ohai_`` will only be present if the ohai_ program is present::

    {
        "ansible_all_ipv4_addresses": [
            "10.0.2.15",
            "192.168.33.10"
        ],
        "ansible_all_ipv6_addresses": [
            "fe80::a00:27ff:fefe:1e4d",
            "fe80::a00:27ff:fe23:ae8e"
        ],
        "ansible_architecture": "x86_64",
        "ansible_bios_date": "12/01/2006",
        "ansible_bios_version": "VirtualBox",
        "ansible_cmdline": {
            "BOOT_IMAGE": "/boot/vmlinuz-3.13.0-35-generic",
            "console": "ttyS0",
            "ro": true,
            "root": "UUID=6e008225-f9bd-4b27-ad0d-e7d323b7a780"
        },
        "ansible_date_time": {
            "date": "2014-12-08",
            "day": "08",
            "epoch": "1418007742",
            "hour": "03",
            "iso8601": "2014-12-08T03:02:22Z",
            "iso8601_micro": "2014-12-08T03:02:22.861624Z",
            "minute": "02",
            "month": "12",
            "second": "22",
            "time": "03:02:22",
            "tz": "UTC",
            "tz_offset": "+0000",
            "weekday": "Monday",
            "year": "2014"
        },
        "ansible_default_ipv4": {
            "address": "10.0.2.15",
            "alias": "eth0",
            "gateway": "10.0.2.2",
            "interface": "eth0",
            "macaddress": "08:00:27:fe:1e:4d",
            "mtu": 1500,
            "netmask": "255.255.255.0",
            "network": "10.0.2.0",
            "type": "ether"
        },
        "ansible_default_ipv6": {},
        "ansible_devices": {
            "sda": {
                "holders": [],
                "host": "SATA controller: Intel Corporation 82801HM/HEM (ICH8M/ICH8M-E) SATA
                         Controller [AHCI mode] (rev 02)",
                "model": "VBOX HARDDISK",
                "partitions": {
                    "sda1": {
                        "sectors": "83884032",
                        "sectorsize": 512,
                        "size": "40.00 GB",
                        "start": "2048"
                    }
                },
                "removable": "0",
                "rotational": "1",
                "scheduler_mode": "deadline",
                "sectors": "83886080",
                "sectorsize": "512",
                "size": "40.00 GB",
                "support_discard": "0",
                "vendor": "ATA"
            }
        },
        "ansible_distribution": "Ubuntu",
        "ansible_distribution_major_version": "14",
        "ansible_distribution_release": "trusty",
        "ansible_distribution_version": "14.04",
        "ansible_domain": "",
        "ansible_env": {
            "HOME": "/home/vagrant",
            "LANG": "en_US.UTF-8",
            "LC_CTYPE": "en_US.UTF-8",
            "LOGNAME": "vagrant",
            "MAIL": "/var/mail/vagrant",
            "PATH": "/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:
                     /usr/local/games",
            "PWD": "/home/vagrant",
            "SHELL": "/bin/bash",
            "SHLVL": "1",
            "SSH_AUTH_SOCK": "/tmp/ssh-FTJFi2Tu1j/agent.12316",
            "SSH_CLIENT": "192.168.33.1 58426 22",
            "SSH_CONNECTION": "192.168.33.1 58426 192.168.33.10 22",
            "USER": "vagrant",
            "XDG_RUNTIME_DIR": "/run/user/1000",
            "XDG_SESSION_ID": "5",
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
            "ipv6": [
                {
                    "address": "fe80::a00:27ff:fefe:1e4d",
                    "prefix": "64",
                    "scope": "link"
                }
            ],
            "macaddress": "08:00:27:fe:1e:4d",
            "module": "e1000",
            "mtu": 1500,
            "promisc": false,
            "type": "ether"
        },
        "ansible_eth1": {
            "active": true,
            "device": "eth1",
            "ipv4": {
                "address": "192.168.33.10",
                "netmask": "255.255.255.0",
                "network": "192.168.33.0"
            },
            "ipv6": [
                {
                    "address": "fe80::a00:27ff:fe23:ae8e",
                    "prefix": "64",
                    "scope": "link"
                }
            ],
            "macaddress": "08:00:27:23:ae:8e",
            "module": "e1000",
            "mtu": 1500,
            "promisc": false,
            "type": "ether"
        },
        "ansible_fips": false,
        "ansible_form_factor": "Other",
        "ansible_fqdn": "vagrant-ubuntu-trusty-64",
        "ansible_hostname": "vagrant-ubuntu-trusty-64",
        "ansible_interfaces": [
            "lo",
            "eth1",
            "eth0"
        ],
        "ansible_kernel": "3.13.0-35-generic",
        "ansible_lo": {
            "active": true,
            "device": "lo",
            "ipv4": {
                "address": "127.0.0.1",
                "netmask": "255.0.0.0",
                "network": "127.0.0.0"
            },
            "ipv6": [
                {
                    "address": "::1",
                    "prefix": "128",
                    "scope": "host"
                }
            ],
            "mtu": 65536,
            "promisc": false,
            "type": "loopback"
        },
        "ansible_lsb": {
            "codename": "trusty",
            "description": "Ubuntu 14.04.1 LTS",
            "id": "Ubuntu",
            "major_release": "14",
            "release": "14.04"
        },
        "ansible_machine": "x86_64",
        "ansible_memfree_mb": 101,
        "ansible_memtotal_mb": 994,
        "ansible_mounts": [
            {
                "device": "/dev/sda1",
                "fstype": "ext4",
                "mount": "/",
                "options": "rw",
                "size_available": 38925029376,
                "size_total": 42241163264
            }
        ],
        "ansible_nodename": "vagrant-ubuntu-trusty-64",
        "ansible_os_family": "Debian",
        "ansible_pkg_mgr": "apt",
        "ansible_processor": [
            "GenuineIntel",
            "Intel(R) Core(TM) i7-4960HQ CPU @ 2.60GHz"
        ],
        "ansible_processor_cores": 1,
        "ansible_processor_count": 1,
        "ansible_processor_threads_per_core": 1,
        "ansible_processor_vcpus": 1,
        "ansible_product_name": "VirtualBox",
        "ansible_product_serial": "NA",
        "ansible_product_uuid": "NA",
        "ansible_product_version": "1.2",
        "ansible_python_version": "2.7.6",
        "ansible_selinux": false,
        "ansible_ssh_host_key_dsa_public":
          "AAAAB3NzaC1kc3MAAACBAJ7d5+Srn6T30vRnMBNnfQNcfSB...",
        "ansible_ssh_host_key_ecdsa_public":
          "AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTY...",
        "ansible_ssh_host_key_rsa_public":
          "AAAAB3NzaC1yc2EAAAADAQABAAABAQDK0HsEEopBN2+N801...",
        "ansible_swapfree_mb": 0,
        "ansible_swaptotal_mb": 0,
        "ansible_system": "Linux",
        "ansible_system_vendor": "innotek GmbH",
        "ansible_user_id": "vagrant",
        "ansible_userspace_architecture": "x86_64",
        "ansible_userspace_bits": "64",
        "ansible_virtualization_role": "guest",
        "ansible_virtualization_type": "virtualbox",
        "facter_architecture": "amd64",
        "facter_augeasversion": "1.2.0",
        "facter_blockdevice_sda_model": "VBOX HARDDISK",
        "facter_blockdevice_sda_size": 42949672960,
        "facter_blockdevice_sda_vendor": "ATA",
        "facter_blockdevices": "sda",
        "facter_facterversion": "1.7.5",
        "facter_filesystems": "ext2,ext3,ext4,vfat",
        "facter_hardwareisa": "x86_64",
        "facter_hardwaremodel": "x86_64",
        "facter_hostname": "vagrant-ubuntu-trusty-64",
        "facter_id": "vagrant",
        "facter_interfaces": "eth0,eth1,lo",
        "facter_ipaddress": "10.0.2.15",
        "facter_ipaddress_eth0": "10.0.2.15",
        "facter_ipaddress_eth1": "192.168.33.10",
        "facter_ipaddress_lo": "127.0.0.1",
        sshdsakey":
          "AAAAB3NzaC1kc3MAAACBAJ7d5+Srn6T30vRnMBNnfQNcfSB...",
        "facter_sshecdsakey":
          "AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTY...",
        "facter_sshfp_dsa":
          "SSHFP 2 1 6b52b74c0ea2bbd5276f7148509bfa0318e55...",
        "facter_sshfp_ecdsa":
          "SSHFP 3 1 d7be510097620ad9f6705c7641ba0d695b73d...",
        "facter_sshfp_rsa":
          "SSHFP 1 1 100db6f684fe47130dfdef5bd1b4e4cda28cb...",
        "facter_sshrsakey":
          "AAAAB3NzaC1yc2EAAAADAQABAAABAQDK0HsEEopBN2+N801...",
        "facter_swapfree": "0.00 MB",
        "facter_swapfree_mb": "0.00",
        "facter_swapsize": "0.00 MB",
        "facter_swapsize_mb": "0.00",
        "facter_timezone": "UTC",
        "facter_uniqueid": "000a0f02",
        "facter_uptime": "0:10 hours",
        "facter_uptime_days": 0,
        "facter_uptime_hours": 0,
        "facter_uptime_seconds": 637,
        "facter_virtual": "virtualbox",
        "module_setup": true,
        "ohai_block_device": {
            "loop0": {
                "removable": "0",
                "size": "0"
            },
            "loop1": {
                "removable": "0",
                "size": "0"
            },
            "loop2": {
                "removable": "0",
                "size": "0"
            },
            "loop3": {
                "removable": "0",
                "size": "0"
            },
            "loop4": {
                "removable": "0",
                "size": "0"
            },
            "loop5": {
                "removable": "0",
                "size": "0"
            },
            "loop6": {
                "removable": "0",
                "size": "0"
            },
            "loop7": {
                "removable": "0",
                "size": "0"
            },
            "ram0": {
                "removable": "0",
                "size": "131072"
            },
            "ram1": {
                "removable": "0",
                "size": "131072"
            },
            "ram10": {
                "removable": "0",
                "size": "131072"
            },
            "ram11": {
                "removable": "0",
                "size": "131072"
            },
            "ram12": {
                "removable": "0",
                "size": "131072"
            },
            "ram13": {
                "removable": "0",
                "size": "131072"
            },
            "ram14": {
                "removable": "0",
                "size": "131072"
            },
            "ram15": {
                "removable": "0",
                "size": "131072"
            },
            "ram2": {
                "removable": "0",
                "size": "131072"
            },
            "ram3": {
                "removable": "0",
                "size": "131072"
            },
            "ram4": {
                "removable": "0",
                "size": "131072"
            },
            "ram5": {
                "removable": "0",
                "size": "131072"
            },
            "ram6": {
                "removable": "0",
                "size": "131072"
            },
            "ram7": {
                "removable": "0",
                "size": "131072"
            },
            "ram8": {
                "removable": "0",
                "size": "131072"
            },
            "ram9": {
                "removable": "0",
                "size": "131072"
            },
            "sda": {
                "model": "VBOX HARDDISK",
                "removable": "0",
                "rev": "1.0",
                "size": "83886080",
                "state": "running",
                "timeout": "30",
                "vendor": "ATA"
            }
        },
        "ohai_chef_packages": {
            "chef": {
                "chef_root": "/usr/lib/ruby/vendor_ruby",
                "version": "11.8.2"
            },
            "ohai": {
                "ohai_root": "/usr/lib/ruby/vendor_ruby/ohai",
                "version": "6.14.0"
            }
        },
        "ohai_command": {
            "ps": "ps -ef"
        },
        "ohai_counters": {
            "network": {
                "interfaces": {
                    "eth0": {
                        "rx": {
                            "bytes": "87120229",
                            "drop": "0",
                            "errors": "0",
                            "overrun": "0",
                            "packets": "95129"
                        },
                        "tx": {
                            "bytes": "2411491",
                            "carrier": "0",
                            "collisions": "0",
                            "drop": "0",
                            "errors": "0",
                            "packets": "38200",
                            "queuelen": "1000"
                        }
                    },
                    "eth1": {
                        "rx": {
                            "bytes": "342365",
                            "drop": "0",
                            "errors": "0",
                            "overrun": "0",
                            "packets": "430"
                        },
                        "tx": {
                            "bytes": "36139",
                            "carrier": "0",
                            "collisions": "0",
                            "drop": "0",
                            "errors": "0",
                            "packets": "218",
                            "queuelen": "1000"
                        }
                    },
                    "lo": {
                        "rx": {
                            "bytes": "761691",
                            "drop": "0",
                            "errors": "0",
                            "overrun": "0",
                            "packets": "2740"
                        },
                        "tx": {
                            "bytes": "761691",
                            "carrier": "0",
                            "collisions": "0",
                            "drop": "0",
                            "errors": "0",
                            "packets": "2740"
                        }
                    }
                }
            }
        },
        "ohai_cpu": {
            "0": {
                "cache_size": "6144 KB",
                "core_id": "0",
                "cores": "1",
                "family": "6",
                "flags": [
                    "fpu",
                    "vme",
                    "de",
                    "pse",
                    "tsc",
                    "msr",
                    "pae",
                    "mce",
                    "cx8",
                    "apic",
                    "sep",
                    "mtrr",
                    "pge",
                    "mca",
                    "cmov",
                    "pat",
                    "pse36",
                    "clflush",
                    "mmx",
                    "fxsr",
                    "sse",
                    "sse2",
                    "syscall",
                    "nx",
                    "rdtscp",
                    "lm",
                    "constant_tsc",
                    "rep_good",
                    "nopl",
                    "pni",
                    "monitor",
                    "ssse3",
                    "lahf_lm"
                ],
                "mhz": "2591.391",
                "model": "70",
                "model_name": "Intel(R) Core(TM) i7-4960HQ CPU @ 2.60GHz",
                "physical_id": "0",
                "stepping": "1",
                "vendor_id": "GenuineIntel"
            },
            "real": 1,
            "total": 1
        },
        "ohai_current_user": "vagrant",
        "ohai_dmi": {
            "dmidecode_version": "2.12"
        },
        "ohai_domain": null,
        "ohai_etc": {
            "group": {
                "adm": {
                    "gid": 4,
                    "members": [
                        "syslog",
                        "ubuntu"
                    ]
                },
                "admin": {
                    "gid": 110,
                    "members": []
                },
                "audio": {
                    "gid": 29,
                    "members": [
                        "ubuntu"
                    ]
                },
                "backup": {
                    "gid": 34,
                    "members": []
                },
                "bin": {
                    "gid": 2,
                    "members": []
                },
                "cdrom": {
                    "gid": 24,
                    "members": [
                        "ubuntu"
                    ]
                },
                "crontab": {
                    "gid": 103,
                    "members": []
                },
                "daemon": {
                    "gid": 1,
                    "members": []
                },
                "dialout": {
                    "gid": 20,
                    "members": [
                        "ubuntu"
                    ]
                },
                "dip": {
                    "gid": 30,
                    "members": [
                        "ubuntu"
                    ]
                },
                "disk": {
                    "gid": 6,
                    "members": []
                },
                "fax": {
                    "gid": 21,
                    "members": []
                },
                "floppy": {
                    "gid": 25,
                    "members": [
                        "ubuntu"
                    ]
                },
                "fuse": {
                    "gid": 105,
                    "members": []
                },
                "games": {
                    "gid": 60,
                    "members": []
                },
                "gnats": {
                    "gid": 41,
                    "members": []
                },
                "irc": {
                    "gid": 39,
                    "members": []
                },
                "kmem": {
                    "gid": 15,
                    "members": []
                },
                "landscape": {
                    "gid": 109,
                    "members": []
                },
                "libuuid": {
                    "gid": 101,
                    "members": []
                },
                "list": {
                    "gid": 38,
                    "members": []
                },
                "lp": {
                    "gid": 7,
                    "members": []
                },
                "mail": {
                    "gid": 8,
                    "members": []
                },
                "man": {
                    "gid": 12,
                    "members": []
                },
                "memcache": {
                    "gid": 113,
                    "members": []
                },
                "messagebus": {
                    "gid": 106,
                    "members": []
                },
                "mlocate": {
                    "gid": 107,
                    "members": []
                },
                "netdev": {
                    "gid": 102,
                    "members": [
                        "ubuntu"
                    ]
                },
                "news": {
                    "gid": 9,
                    "members": []
                },
                "nogroup": {
                    "gid": 65534,
                    "members": []
                },
                "operator": {
                    "gid": 37,
                    "members": []
                },
                "plugdev": {
                    "gid": 46,
                    "members": [
                        "ubuntu"
                    ]
                },
                "postgres": {
                    "gid": 115,
                    "members": []
                },
                "proxy": {
                    "gid": 13,
                    "members": []
                },
                "puppet": {
                    "gid": 112,
                    "members": []
                },
                "root": {
                    "gid": 0,
                    "members": []
                },
                "sasl": {
                    "gid": 45,
                    "members": []
                },
                "shadow": {
                    "gid": 42,
                    "members": []
                },
                "src": {
                    "gid": 40,
                    "members": []
                },
                "ssh": {
                    "gid": 108,
                    "members": []
                },
                "ssl-cert": {
                    "gid": 114,
                    "members": [
                        "postgres"
                    ]
                },
                "staff": {
                    "gid": 50,
                    "members": []
                },
                "sudo": {
                    "gid": 27,
                    "members": [
                        "ubuntu"
                    ]
                },
                "sys": {
                    "gid": 3,
                    "members": []
                },
                "syslog": {
                    "gid": 104,
                    "members": []
                },
                "tape": {
                    "gid": 26,
                    "members": []
                },
                "tty": {
                    "gid": 5,
                    "members": []
                },
                "ubuntu": {
                    "gid": 1001,
                    "members": []
                },
                "users": {
                    "gid": 100,
                    "members": []
                },
                "utmp": {
                    "gid": 43,
                    "members": []
                },
                "uucp": {
                    "gid": 10,
                    "members": []
                },
                "vagrant": {
                    "gid": 1000,
                    "members": []
                },
                "vboxsf": {
                    "gid": 111,
                    "members": []
                },
                "video": {
                    "gid": 44,
                    "members": [
                        "ubuntu"
                    ]
                },
                "voice": {
                    "gid": 22,
                    "members": []
                },
                "www-data": {
                    "gid": 33,
                    "members": []
                }
            },
            "passwd": {
                "backup": {
                    "dir": "/var/backups",
                    "gecos": "backup",
                    "gid": 34,
                    "shell": "/usr/sbin/nologin",
                    "uid": 34
                },
                "bin": {
                    "dir": "/bin",
                    "gecos": "bin",
                    "gid": 2,
                    "shell": "/usr/sbin/nologin",
                    "uid": 2
                },
                "daemon": {
                    "dir": "/usr/sbin",
                    "gecos": "daemon",
                    "gid": 1,
                    "shell": "/usr/sbin/nologin",
                    "uid": 1
                },
                "games": {
                    "dir": "/usr/games",
                    "gecos": "games",
                    "gid": 60,
                    "shell": "/usr/sbin/nologin",
                    "uid": 5
                },
                "gnats": {
                    "dir": "/var/lib/gnats",
                    "gecos": "Gnats Bug-Reporting System (admin)",
                    "gid": 41,
                    "shell": "/usr/sbin/nologin",
                    "uid": 41
                },
                "irc": {
                    "dir": "/var/run/ircd",
                    "gecos": "ircd",
                    "gid": 39,
                    "shell": "/usr/sbin/nologin",
                    "uid": 39
                },
                "landscape": {
                    "dir": "/var/lib/landscape",
                    "gecos": "",
                    "gid": 109,
                    "shell": "/bin/false",
                    "uid": 103
                },
                "libuuid": {
                    "dir": "/var/lib/libuuid",
                    "gecos": "",
                    "gid": 101,
                    "shell": "",
                    "uid": 100
                },
                "list": {
                    "dir": "/var/list",
                    "gecos": "Mailing List Manager",
                    "gid": 38,
                    "shell": "/usr/sbin/nologin",
                    "uid": 38
                },
                "lp": {
                    "dir": "/var/spool/lpd",
                    "gecos": "lp",
                    "gid": 7,
                    "shell": "/usr/sbin/nologin",
                    "uid": 7
                },
                "mail": {
                    "dir": "/var/mail",
                    "gecos": "mail",
                    "gid": 8,
                    "shell": "/usr/sbin/nologin",
                    "uid": 8
                },
                "man": {
                    "dir": "/var/cache/man",
                    "gecos": "man",
                    "gid": 12,
                    "shell": "/usr/sbin/nologin",
                    "uid": 6
                },
                "memcache": {
                    "dir": "/nonexistent",
                    "gecos": "Memcached,,,",
                    "gid": 113,
                    "shell": "/bin/false",
                    "uid": 108
                },
                "messagebus": {
                    "dir": "/var/run/dbus",
                    "gecos": "",
                    "gid": 106,
                    "shell": "/bin/false",
                    "uid": 102
                },
                "news": {
                    "dir": "/var/spool/news",
                    "gecos": "news",
                    "gid": 9,
                    "shell": "/usr/sbin/nologin",
                    "uid": 9
                },
                "nobody": {
                    "dir": "/nonexistent",
                    "gecos": "nobody",
                    "gid": 65534,
                    "shell": "/usr/sbin/nologin",
                    "uid": 65534
                },
                "pollinate": {
                    "dir": "/var/cache/pollinate",
                    "gecos": "",
                    "gid": 1,
                    "shell": "/bin/false",
                    "uid": 105
                },
                "postgres": {
                    "dir": "/var/lib/postgresql",
                    "gecos": "PostgreSQL administrator,,,",
                    "gid": 115,
                    "shell": "/bin/bash",
                    "uid": 109
                },
                "proxy": {
                    "dir": "/bin",
                    "gecos": "proxy",
                    "gid": 13,
                    "shell": "/usr/sbin/nologin",
                    "uid": 13
                },
                "puppet": {
                    "dir": "/var/lib/puppet",
                    "gecos": "Puppet configuration management daemon,,,",
                    "gid": 112,
                    "shell": "/bin/false",
                    "uid": 107
                },
                "root": {
                    "dir": "/root",
                    "gecos": "root",
                    "gid": 0,
                    "shell": "/bin/bash",
                    "uid": 0
                },
                "sshd": {
                    "dir": "/var/run/sshd",
                    "gecos": "",
                    "gid": 65534,
                    "shell": "/usr/sbin/nologin",
                    "uid": 104
                },
                "statd": {
                    "dir": "/var/lib/nfs",
                    "gecos": "",
                    "gid": 65534,
                    "shell": "/bin/false",
                    "uid": 106
                },
                "sync": {
                    "dir": "/bin",
                    "gecos": "sync",
                    "gid": 65534,
                    "shell": "/bin/sync",
                    "uid": 4
                },
                "sys": {
                    "dir": "/dev",
                    "gecos": "sys",
                    "gid": 3,
                    "shell": "/usr/sbin/nologin",
                    "uid": 3
                },
                "syslog": {
                    "dir": "/home/syslog",
                    "gecos": "",
                    "gid": 104,
                    "shell": "/bin/false",
                    "uid": 101
                },
                "ubuntu": {
                    "dir": "/home/ubuntu",
                    "gecos": "Ubuntu",
                    "gid": 1001,
                    "shell": "/bin/bash",
                    "uid": 1001
                },
                "uucp": {
                    "dir": "/var/spool/uucp",
                    "gecos": "uucp",
                    "gid": 10,
                    "shell": "/usr/sbin/nologin",
                    "uid": 10
                },
                "vagrant": {
                    "dir": "/home/vagrant",
                    "gecos": "",
                    "gid": 1000,
                    "shell": "/bin/bash",
                    "uid": 1000
                },
                "www-data": {
                    "dir": "/var/www",
                    "gecos": "www-data",
                    "gid": 33,
                    "shell": "/usr/sbin/nologin",
                    "uid": 33
                }
            }
        },
        "ohai_filesystem": {
            "/dev/disk/by-uuid/6e008225-f9bd-4b27-ad0d-e7d323b7a780": {
                "fs_type": "ext4",
                "mount": "/",
                "mount_options": [
                    "rw",
                    "relatime",
                    "data=ordered"
                ]
            },
            "/dev/sda1": {
                "fs_type": "ext4",
                "kb_available": "38012724",
                "kb_size": "41251136",
                "kb_used": "1502500",
                "label": "cloudimg-rootfs",
                "mount": "/",
                "mount_options": [
                    "rw"
                ],
                "percent_used": "4%",
                "uuid": "6e008225-f9bd-4b27-ad0d-e7d323b7a780"
            },
            "devpts": {
                "fs_type": "devpts",
                "mount": "/dev/pts",
                "mount_options": [
                    "rw",
                    "noexec",
                    "nosuid",
                    "gid=5",
                    "mode=0620"
                ]
            },
            "none": {
                "fs_type": "pstore",
                "kb_available": "102400",
                "kb_size": "102400",
                "kb_used": "0",
                "mount": "/sys/fs/pstore",
                "mount_options": [
                    "rw"
                ],
                "percent_used": "0%"
            },
            "proc": {
                "fs_type": "proc",
                "mount": "/proc",
                "mount_options": [
                    "rw",
                    "noexec",
                    "nosuid",
                    "nodev"
                ]
            },
            "rootfs": {
                "fs_type": "rootfs",
                "mount": "/",
                "mount_options": [
                    "rw"
                ]
            },
            "rpc_pipefs": {
                "fs_type": "rpc_pipefs",
                "mount": "/run/rpc_pipefs",
                "mount_options": [
                    "rw"
                ]
            },
            "sysfs": {
                "fs_type": "sysfs",
                "mount": "/sys",
                "mount_options": [
                    "rw",
                    "noexec",
                    "nosuid",
                    "nodev"
                ]
            },
            "systemd": {
                "fs_type": "cgroup",
                "mount": "/sys/fs/cgroup/systemd",
                "mount_options": [
                    "rw",
                    "noexec",
                    "nosuid",
                    "nodev",
                    "none",
                    "name=systemd"
                ]
            },
            "tmpfs": {
                "fs_type": "tmpfs",
                "kb_available": "101416",
                "kb_size": "101788",
                "kb_used": "372",
                "mount": "/run",
                "mount_options": [
                    "rw",
                    "noexec",
                    "nosuid",
                    "size=10%",
                    "mode=0755"
                ],
                "percent_used": "1%"
            },
            "udev": {
                "fs_type": "devtmpfs",
                "kb_available": "503952",
                "kb_size": "503964",
                "kb_used": "12",
                "mount": "/dev",
                "mount_options": [
                    "rw",
                    "mode=0755"
                ],
                "percent_used": "1%"
            },
            "vagrant": {
                "fs_type": "vboxsf",
                "kb_available": "305450008",
                "kb_size": "487385240",
                "kb_used": "181935232",
                "mount": "/vagrant",
                "mount_options": [
                    "uid=1000",
                    "gid=1000",
                    "rw"
                ],
                "percent_used": "38%"
            }
        },
        "ohai_fqdn": "vagrant-ubuntu-trusty-64",
        "ohai_hostname": "vagrant-ubuntu-trusty-64",
        "ohai_idletime": "9 minutes 26 seconds",
        "ohai_idletime_seconds": 566,
        "ohai_ipaddress": "10.0.2.15",
        "ohai_kernel": {
            "machine": "x86_64",
            "modules": {
                "ahci": {
                    "refcount": "1",
                    "size": "25819"
                },
                "auth_rpcgss": {
                    "refcount": "1",
                    "size": "59338"
                },
                "dm_crypt": {
                    "refcount": "0",
                    "size": "23177"
                },
                "e1000": {
                    "refcount": "0",
                    "size": "145174"
                },
                "fscache": {
                    "refcount": "1",
                    "size": "63988"
                },
                "libahci": {
                    "refcount": "1",
                    "size": "32716"
                },
                "lockd": {
                    "refcount": "2",
                    "size": "93977"
                },
                "nfs": {
                    "refcount": "0",
                    "size": "236636"
                },
                "nfs_acl": {
                    "refcount": "1",
                    "size": "12837"
                },
                "nfsd": {
                    "refcount": "2",
                    "size": "280289"
                },
                "parport": {
                    "refcount": "2",
                    "size": "42348"
                },
                "parport_pc": {
                    "refcount": "0",
                    "size": "32701"
                },
                "ppdev": {
                    "refcount": "0",
                    "size": "17671"
                },
                "psmouse": {
                    "refcount": "0",
                    "size": "106678"
                },
                "serio_raw": {
                    "refcount": "0",
                    "size": "13462"
                },
                "sunrpc": {
                    "refcount": "6",
                    "size": "284939"
                },
                "vboxguest": {
                    "refcount": "2",
                    "size": "248441"
                },
                "vboxsf": {
                    "refcount": "1",
                    "size": "43786"
                }
            },
            "name": "Linux",
            "os": "GNU/Linux",
            "release": "3.13.0-35-generic",
            "version": "#62-Ubuntu SMP Fri Aug 15 01:58:42 UTC 2014"
        },
        "ohai_keys": {
            "ssh": {
                "host_dsa_public": "AAAAB3NzaC1kc3MAAACBAJ7d5+Srn6T30...",
                "host_rsa_public": "AAAAB3NzaC1yc2EAAAADAQABAAABAQDK0..."
            }
        },
        "ohai_languages": {
            "perl": {
                "archname": "x86_64-linux-gnu-thread-multi",
                "version": "5.18.2"
            },
            "python": {
                "builddate": "Mar 22 2014, 22:59:56",
                "version": "2.7.6"
            },
            "ruby": {
                "bin_dir": "/usr/bin",
                "gem_bin": "/usr/bin/gem1.9.1",
                "gems_dir": "/var/lib/gems/1.9.1",
                "host": "x86_64-pc-linux-gnu",
                "host_cpu": "x86_64",
                "host_os": "linux-gnu",
                "host_vendor": "pc",
                "platform": "x86_64-linux",
                "release_date": "2013-11-22",
                "ruby_bin": "/usr/bin/ruby1.9.1",
                "target": "x86_64-pc-linux-gnu",
                "target_cpu": "x86_64",
                "target_os": "linux",
                "target_vendor": "pc",
                "version": "1.9.3"
            }
        },
        "ohai_lsb": {
            "codename": "trusty",
            "description": "Ubuntu 14.04.1 LTS",
            "id": "Ubuntu",
            "release": "14.04"
        },
        "ohai_macaddress": "08:00:27:FE:1E:4D",
        "ohai_memory": {
            "active": "548644kB",
            "anon_pages": "212420kB",
            "bounce": "0kB",
            "buffers": "60088kB",
            "cached": "551148kB",
            "commit_limit": "508928kB",
            "committed_as": "488724kB",
            "dirty": "100kB",
            "free": "91524kB",
            "inactive": "275012kB",
            "mapped": "29856kB",
            "nfs_unstable": "0kB",
            "page_tables": "6036kB",
            "slab": "82572kB",
            "slab_reclaimable": "72836kB",
            "slab_unreclaim": "9736kB",
            "swap": {
                "cached": "0kB",
                "free": "0kB",
                "total": "0kB"
            },
            "total": "1017856kB",
            "vmalloc_chunk": "34359715831kB",
            "vmalloc_total": "34359738367kB",
            "vmalloc_used": "18700kB",
            "writeback": "0kB"
        },
        "ohai_network": {
            "default_gateway": "10.0.2.2",
            "default_interface": "eth0",
            "interfaces": {
                "eth0": {
                    "addresses": {
                        "08:00:27:FE:1E:4D": {
                            "family": "lladdr"
                        },
                        "10.0.2.15": {
                            "broadcast": "10.0.2.255",
                            "family": "inet",
                            "netmask": "255.255.255.0",
                            "prefixlen": "24",
                            "scope": "Global"
                        },
                        "fe80::a00:27ff:fefe:1e4d": {
                            "family": "inet6",
                            "prefixlen": "64",
                            "scope": "Link"
                        }
                    },
                    "arp": {
                        "10.0.2.2": "52:54:00:12:35:02",
                        "10.0.2.3": "52:54:00:12:35:03"
                    },
                    "encapsulation": "Ethernet",
                    "flags": [
                        "BROADCAST",
                        "MULTICAST",
                        "UP",
                        "LOWER_UP"
                    ],
                    "mtu": "1500",
                    "number": "0",
                    "routes": [
                        {
                            "destination": "default",
                            "family": "inet",
                            "via": "10.0.2.2"
                        },
                        {
                            "destination": "10.0.2.0/24",
                            "family": "inet",
                            "proto": "kernel",
                            "scope": "link",
                            "src": "10.0.2.15"
                        },
                        {
                            "destination": "fe80::/64",
                            "family": "inet6",
                            "metric": "256",
                            "proto": "kernel"
                        }
                    ],
                    "state": "up",
                    "type": "eth"
                },
                "eth1": {
                    "addresses": {
                        "08:00:27:23:AE:8E": {
                            "family": "lladdr"
                        },
                        "192.168.33.10": {
                            "broadcast": "192.168.33.255",
                            "family": "inet",
                            "netmask": "255.255.255.0",
                            "prefixlen": "24",
                            "scope": "Global"
                        },
                        "fe80::a00:27ff:fe23:ae8e": {
                            "family": "inet6",
                            "prefixlen": "64",
                            "scope": "Link"
                        }
                    },
                    "arp": {
                        "192.168.33.1": "0a:00:27:00:00:00"
                    },
                    "encapsulation": "Ethernet",
                    "flags": [
                        "BROADCAST",
                        "MULTICAST",
                        "UP",
                        "LOWER_UP"
                    ],
                    "mtu": "1500",
                    "number": "1",
                    "routes": [
                        {
                            "destination": "192.168.33.0/24",
                            "family": "inet",
                            "proto": "kernel",
                            "scope": "link",
                            "src": "192.168.33.10"
                        },
                        {
                            "destination": "fe80::/64",
                            "family": "inet6",
                            "metric": "256",
                            "proto": "kernel"
                        }
                    ],
                    "state": "up",
                    "type": "eth"
                },
                "lo": {
                    "addresses": {
                        "127.0.0.1": {
                            "family": "inet",
                            "netmask": "255.0.0.0",
                            "prefixlen": "8",
                            "scope": "Node"
                        },
                        "::1": {
                            "family": "inet6",
                            "prefixlen": "128",
                            "scope": "Node"
                        }
                    },
                    "encapsulation": "Loopback",
                    "flags": [
                        "LOOPBACK",
                        "UP",
                        "LOWER_UP"
                    ],
                    "mtu": "65536",
                    "state": "unknown"
                }
            },
            "listeners": {
                "tcp": {
                    "111": {
                        "address": "*",
                        "pid": 0
                    },
                    "11211": {
                        "address": "127.0.0.1",
                        "pid": 0
                    },
                    "22": {
                        "address": "*",
                        "name": "gunicorn: maste",
                        "pid": 0
                    },
                    "443": {
                        "address": "*",
                        "name": "",
                        "pid": 0
                    },
                    "49788": {
                        "address": "*",
                        "name": "gunicorn: maste",
                        "pid": 0
                    },
                    "50583": {
                        "address": "*",
                        "name": "",
                        "pid": 0
                    },
                    "5432": {
                        "address": "127.0.0.1",
                        "name": "",
                        "pid": 0
                    },
                    "80": {
                        "address": "*",
                        "name": "",
                        "pid": 0
                    },
                    "8000": {
                        "address": "127.0.0.1",
                        "name": "gunicorn: maste",
                        "pid": 9601
                    }
                }
            }
        },
        "ohai_ohai_time": 1418007743.6774073,
        "ohai_os": "linux",
        "ohai_os_version": "3.13.0-35-generic",
        "ohai_platform": "ubuntu",
        "ohai_platform_family": "debian",
        "ohai_platform_version": "14.04",
        "ohai_uptime": "10 minutes 37 seconds",
        "ohai_uptime_seconds": 637,
        "ohai_virtualization": {
            "role": "guest",
            "system": "vbox"
        }
    }


.. _facter: https://docs.puppetlabs.com/facter/

.. _ohai: https://docs.chef.io/ohai.html
