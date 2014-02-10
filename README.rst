===============
Quick reference
===============

Quick reference to parameters and special variables.


Built-in variables
==================

These are variables that are always defined by ansible.

============================   =========================================================================================================================================================================================================
Parameter                      Description
============================   =========================================================================================================================================================================================================
groups                         A dict whose keys are Ansible group names and values are list of hostnames that are members of the group. Includes ``all`` and ``ungrouped`` groups: ``{"all": [...], "web": [...], "ungrouped": [...]}``
inventory_hostname             Name of the current host as known by ansible.
============================   =========================================================================================================================================================================================================

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



Play parameters
---------------

===================  =======================================================================
Parameter            Description
===================  =======================================================================
name                 Name of the play, displayed when play runs (e.g., ``Deploy a foo``).
hosts                Hosts in the play (e.g., ``webservers``).
vars                 Dictionary of variables.
vars_files           List of files that contain dictionary of variables.
vars_prompt          Description of vars that user will be prompted to specify.
user                 User to ssh as. Default: ``root`` (unless overriden in config file)
remote_user          Alias for ``user``.
sudo                 Boolean that indicates whether ansible should use sudo (e.g., ``True``).
sudo_user            If sudo'ing, user to sudo as. Defaults: ``root``.
tasks                List of tasks.
roles                List of roles.
pre_tasks            List of tasks to execute before roles.
post_tasks           List of tasks to execute after roles.
serial               Integer that indicates how many hosts Ansible should manage at a single
                     time. (e.g., ``3``).
max_fail_percentage
===================  =======================================================================

Task parameters
===============

==================  =========================================================================================
Parameter           Description
==================  =========================================================================================
name                Name of the task, displayed when task runs (e.g., ``Ensure foo is present``).
action              Name of module to specify. Legacy format, prefer specifying module name directly instead
include             Name of a separate YAML file that includes additional tasks.
register            Record the result to the specified variable (e.g., ``result``)
delegate_to         Run task on specified host instead.
local_action        Equivalent to: ``delegate_to: 127.0.0.1``.
user                User to ssh as for this task
sudo                Boolean that indicates whether ansible should use sudo on this task
sudo_user           If sudo'ing, user to sudo as.
when                Boolean. Only run task when this evaluates to True. Default: ``True``
ignore_errors       Boolean. If True, ansible will treat task as if it has succeeded even if it returned an
                    error, Default: ``False``
module              More verbose notation for specifying module parameters
environment         Mapping that contains environment variables to pass
failed_when         Specify criteria for identifying task has failed (e.g., ``"'FAILED' in command_result.stderr"``)
with_items          List of items to iterate over
with_nested         List of list of items to iterate over in nested fashion
with_fileglob       List of local files to iterate over, described using shell fileglob notation
                    (e.g., ``/playbooks/files/fooapp/*``)
with_first_found    tbd
with_together       Dictionary of lists to iterate over in parallel
with_random_choice  List of items to be selected from at random
until               Boolean, task will retry until evaluates true or until ``retries``
retries             Used with "until", number of times to retry. Default: ``3``
delay               Used with "until", seconds to wait between retries. Default: ``10``

==================  =========================================================================================



Host variables that modify ansible behavior
===========================================

============================   =========================================================================================
Parameter                      Description
============================   =========================================================================================
ansible_ssh_host               hostname to connect to for a given host
ansible_ssh_port               ssh port to connect to for a given host
ansible_ssh_user               ssh user to connect as for a given host
ansible_ssh_pass               ssh password to connect as for a given host
ansible_ssh_private_key_file   ssh private key file to connect as for a given host
ansible_connection             connection type to use for a given host (e.g. ``local``)
ansible_python_interpreter     python interpreter to use
ansible\_\*\_interpreter       interpreter to use
============================   =========================================================================================



Variables returned by setup
===========================

=================              ==================================================                  =====================================================================================================================================================================================================================================================
Parameter                      Description                                                         Example
=================              ==================================================                  =====================================================================================================================================================================================================================================================
ansible_date_time              Dictionary that contains date info                                  ``{"date": "2013-10-02", "day": "02", "epoch": "1380756810", "hour": "19","iso8601": "2013-10-02T23:33:30Z","iso8601_micro": "2013-10-02T23:33:30.036070Z","minute": "33","month": "10","second": "30","time": "19:33:30","tz": "EDT","year": "2013"}``
=================              ==================================================                  =====================================================================================================================================================================================================================================================


EC2 stuff
=========


Values returned by ec2 module
------------------------------

===================  =======================================================================
Parameter            Description
===================  =======================================================================
instance_ids         List of instance ids
instances            List of instance dicts (see table below)
===================  =======================================================================

EC2 instance dicts
~~~~~~~~~~~~~~~~~~

===================  =======================================================================
Parameter            Description
===================  =======================================================================
id                   instance id
ami_launch_index     tbd
private_ip           internal IP address (not routable outside of EC2)
private_dns_name     internal DNS name (not routable outside of EC2)
public_ip            public IP address
public_dns_name      public DNS name
state_code           tbd
architecture         CPU architecture
image_id             AMI
key_name             keypair name
placement            tbd
kernel               AKI
ramdisk              ARI
launch_time          time instance was launched
instance_type        instance type
root_device_type     type of root device (ephemeral, EBS)
root_device_name     name of root device
state                state of instance
hypervisor           hypervisor type
===================  =======================================================================


Values returned by ec2_facts module
-----------------------------------

This will connect to the EC2 metadata service and set the variables, prefixed
with ``ansible_ec2_``. Any variable that has a dash (``-``)  or colon (``:``) in
the name will also have a copied version of that variable with underscores
instead (e.g., ``ansible_ec2_ami-id`` and ``ansible_ec2_ami_id``).

Here we just show the underscore-replaced versions


=====================================================================  =======================================================================
Parameter                                                              Description
=====================================================================  =======================================================================
ansible_ec2_ami_launch_index                                           ? (e.g., `0`)
ansible_ec2_ami_manifest_path                                          ? (e.g., `(unknown)`)
ansible_ec2_hostname                                                   hostname
ansible_ec2_instance_action                                            tbd
ansible_ec2_instance_id                                                instance id
ansible_ec2_instance_type                                              instance type
ansible_ec2_kernel_id                                                  AKI
ansible_ec2_local_hostname                                             internal hostname
ansible_ec2_local_ipv4                                                 internal IP address
ansible_ec2_mac                                                        MAC address (e.g., ``22:00:0a:1f:b2:34``)
ansible_ec2_network_interfaces_macs_XX_XX_XX_XX_XX_XX_device_number    device number (e.g., ``0``)
ansible_ec2_network_interfaces_macs_XX_XX_XX_XX_XX_XX_local_hostname   internal hostname for interface (e.g., ``ip-10-31-178-52.ec2.internal``)
ansible_ec2_network_interfaces_macs_XX_XX_XX_XX_XX_XX_local_ipv4s      internal IP for interface (e.g., ``10.31.178.52``)
ansible_ec2_network_interfaces_macs_XX_XX_XX_XX_XX_XX_mac              MAC  address (e.g., ``22:00:0a:1f:b2:34``)
ansible_ec2_network_interfaces_macs_XX_XX_XX_XX_XX_XX_owner_id         Owner ID (e.g., ``635425997824``)
ansible_ec2_network_interfaces_macs_XX_XX_XX_XX_XX_XX_public_hostname  public hostname (e.g., ``ec2-107-20-42-224.compute-1.amazonaws.com``)
ansible_ec2_network_interfaces_macs_XX_XX_XX_XX_XX_XX_public_ipv4s"    public IP (e.g., ``107.20.42.224``)
ansible_ec2_public_hostname                                            public hostname (e.g., ``ec2-107-20-42-224.compute-1.amazonaws.com``)
ansible_ec2_public_key                                                 ssh public key
ansible_ec2_public_ipv4                                                public IP address (e.g., ``107.20.42.224``)
ansible_ec2_reservation_id                                             reservation id
ansible_ec2_security_groups                                            comma-delimited list of security groups (e.g., ``ssh,ping``)
ansible_ec2_instance_type                                              instance type (e.g., ``t1.micro``)
ansible_ec2_placement_availability_zone                                availability zone (e.g., ``us-east-1b``)
ansible_ec2_placement_region                                           region (e.g., ``us-east-1``)
ansible_ec2_profile                                                    profile (e.g. ``default-paravitual``)
ansible_ec2_user_data                                                  user data
=====================================================================  =======================================================================

Values returned by ec2_ami module
-----------------------------------

===================  =======================================================================
Parameter            Description
===================  =======================================================================
image_id             AMI id
state                state of the image
===================  =======================================================================
