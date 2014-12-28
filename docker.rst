Docker stuff
============

.. _docker:

Values returned by docker module
--------------------------------

The Docker module sets facts, so there's no need to use `register` in order to
access these variables. Instead, just access the `docker_containers` variable,
which is a list that looks like this::

    "docker_containers": [
        {
            "AppArmorProfile": "",
            "Args": [
                "postgres"
            ],
            "Config": {
                "AttachStderr": false,
                "AttachStdin": false,
                "AttachStdout": false,
                "Cmd": [
                    "postgres"
                ],
                "CpuShares": 0,
                "Cpuset": "",
                "Domainname": "",
                "Entrypoint": [
                    "/docker-entrypoint.sh"
                ],
                "Env": [
                    "POSTGRES_PASSWORD=password",
                    "POSTGRES_USER=mezzanine",
                    "PATH=/usr/lib/postgresql/9.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                    "LANG=en_US.utf8",
                    "PG_MAJOR=9.4",
                    "PG_VERSION=9.4.0-1.pgdg70+1",
                    "PGDATA=/var/lib/postgresql/data"
                ],
                "ExposedPorts": {
                    "5432/tcp": {}
                },
                "Hostname": "71f40ec4b58c",
                "Image": "postgres",
                "MacAddress": "",
                "Memory": 0,
                "MemorySwap": 0,
                "NetworkDisabled": false,
                "OnBuild": null,
                "OpenStdin": false,
                "PortSpecs": null,
                "StdinOnce": false,
                "Tty": false,
                "User": "",
                "Volumes": {
                    "/var/lib/postgresql/data": {}
                },
                "WorkingDir": ""
            },
            "Created": "2014-12-25T22:59:15.841107151Z",
            "Driver": "aufs",
            "ExecDriver": "native-0.2",
            "HostConfig": {
                "Binds": null,
                "CapAdd": null,
                "CapDrop": null,
                "ContainerIDFile": "",
                "Devices": null,
                "Dns": null,
                "DnsSearch": null,
                "ExtraHosts": null,
                "IpcMode": "",
                "Links": null,
                "LxcConf": null,
                "NetworkMode": "",
                "PortBindings": {
                    "5432/tcp": [
                        {
                            "HostIp": "0.0.0.0",
                            "HostPort": ""
                        }
                    ]
                },
                "Privileged": false,
                "PublishAllPorts": false,
                "RestartPolicy": {
                    "MaximumRetryCount": 0,
                    "Name": ""
                },
                "SecurityOpt": null,
                "VolumesFrom": [
                    "data-volume"
                ]
            },
            "HostnamePath": "/mnt/sda1/var/lib/docker/containers/71f40ec4b58c3176030274afb025fbd3eb130fe79d4a6a69de473096f335e7eb/hostname",
            "HostsPath": "/mnt/sda1/var/lib/docker/containers/71f40ec4b58c3176030274afb025fbd3eb130fe79d4a6a69de473096f335e7eb/hosts",
            "Id": "71f40ec4b58c3176030274afb025fbd3eb130fe79d4a6a69de473096f335e7eb",
            "Image": "b58a816df10fb20c956d39724001d4f2fabddec50e0d9099510f0eb579ec8a45",
            "MountLabel": "",
            "Name": "/high_lovelace",
            "NetworkSettings": {
                "Bridge": "docker0",
                "Gateway": "172.17.42.1",
                "IPAddress": "172.17.0.12",
                "IPPrefixLen": 16,
                "MacAddress": "02:42:ac:11:00:0c",
                "PortMapping": null,
                "Ports": {
                    "5432/tcp": [
                        {
                            "HostIp": "0.0.0.0",
                            "HostPort": "49153"
                        }
                    ]
                }
            },
            "Path": "/docker-entrypoint.sh",
            "ProcessLabel": "",
            "ResolvConfPath": "/mnt/sda1/var/lib/docker/containers/71f40ec4b58c3176030274afb025fbd3eb130fe79d4a6a69de473096f335e7eb/resolv.conf",
            "State": {
                "Error": "",
                "ExitCode": 0,
                "FinishedAt": "0001-01-01T00:00:00Z",
                "OOMKilled": false,
                "Paused": false,
                "Pid": 9625,
                "Restarting": false,
                "Running": true,
                "StartedAt": "2014-12-25T22:59:16.219732465Z"
            },
            "Volumes": {
                "/var/lib/postgresql/data": "/mnt/sda1/var/lib/docker/vfs/dir/4ccd3150c8d74b9b0feb56df928ac915599e12c3ab573cd4738a18fe3dc6f474"
            },
            "VolumesRW": {
                "/var/lib/postgresql/data": true
            }
        }
    ]
