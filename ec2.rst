EC2 stuff
=========

.. _ec2:

* `Values returned by EC2 module <#values-returned-by-ec2-module>`_

  + `EC2 instance dicts <#ec2-instance-dicts>`_

* `Values returned by ec2_vpc module <#values-returned-by-ec2_vpc-module>`_

  + `subnet dict <#subnet-dict>`_
  + `vpc dict <#vpc-dict>`_

* `hostvars from ec2.py dynamic inventory script <#hostvars-from-ec2py-dynamic-inventory-script>`_
* `Values returned by ec2_facts module <#values-returned-by-ec2_facts-module>`_
* `Values returned by ec2_ami module <#values-returned-by-ec2_ami-module>`_ 
* `Values returned by ec2_vol module <#values-returned-by-ec2_vol-module>`_ 
* `Values returned by ec2_key module <#values-returned-by-ec2_key-module>`_ 


Values returned by ec2 module
------------------------------

This assumes you're using tagging.


If the instances don't exist yet::

 {
        "changed": false,
        "instance_ids": [
           "i-db2fd037",
        ],
        "instances": [
            {
                "ami_launch_index": "0",
                "architecture": "x86_64",
                "dns_name": "ec2-54-173-62-41.compute-1.amazonaws.com",
                "ebs_optimized": false,
                "hypervisor": "xen",
                "id": "i-db2fd037",
                "image_id": "ami-9aaa1cf2",
                "instance_type": "t2.micro",
                "kernel": null,
                "key_name": "mykey",
                "launch_time": "2014-11-16T03:53:31.000Z",
                "placement": "us-east-1d",
                "private_dns_name": "ip-10-0-0-17.ec2.internal",
                "private_ip": "10.0.0.17",
                "public_dns_name": "ec2-54-173-62-41.compute-1.amazonaws.com",
                "public_ip": "54.173.62.41",
                "ramdisk": null,
                "region": "us-east-1",
                "root_device_name": "/dev/sda1",
                "root_device_type": "ebs",
                "state": "running",
                "state_code": 16,
                "virtualization_type": "hvm"
            }
        ]
        "invocation": {
            "module_args": "",
            "module_name": "ec2"
        },
        "tagged_instances": [
            {
                "ami_launch_index": "0",
                "architecture": "x86_64",
                "dns_name": "ec2-54-173-62-41.compute-1.amazonaws.com",
                "ebs_optimized": false,
                "hypervisor": "xen",
                "id": "i-db2fd037",
                "image_id": "ami-9aaa1cf2",
                "instance_type": "t2.micro",
                "kernel": null,
                "key_name": "mykey",
                "launch_time": "2014-11-16T03:53:31.000Z",
                "placement": "us-east-1d",
                "private_dns_name": "ip-10-0-0-17.ec2.internal",
                "private_ip": "10.0.0.17",
                "public_dns_name": "ec2-54-173-62-41.compute-1.amazonaws.com",
                "public_ip": "54.173.62.41",
                "ramdisk": null,
                "region": "us-east-1",
                "root_device_name": "/dev/sda1",
                "root_device_type": "ebs",
                "state": "running",
                "state_code": 16,
                "virtualization_type": "hvm"
            }
        ]
    }

If the instances already exist::

 {
        "changed": false,
        "instance_ids": null,
        "instances": null,
        "invocation": {
            "module_args": "",
            "module_name": "ec2"
        },
        "tagged_instances": [
            {
                "ami_launch_index": "0",
                "architecture": "x86_64",
                "dns_name": "ec2-54-173-62-41.compute-1.amazonaws.com",
                "ebs_optimized": false,
                "hypervisor": "xen",
                "id": "i-db2fd037",
                "image_id": "ami-9aaa1cf2",
                "instance_type": "t2.micro",
                "kernel": null,
                "key_name": "mykey",
                "launch_time": "2014-11-16T03:53:31.000Z",
                "placement": "us-east-1d",
                "private_dns_name": "ip-10-0-0-17.ec2.internal",
                "private_ip": "10.0.0.17",
                "public_dns_name": "ec2-54-173-62-41.compute-1.amazonaws.com",
                "public_ip": "54.173.62.41",
                "ramdisk": null,
                "region": "us-east-1",
                "root_device_name": "/dev/sda1",
                "root_device_type": "ebs",
                "state": "running",
                "state_code": 16,
                "virtualization_type": "hvm"
            }
        ]
    }

===================  =======================================================================
Parameter            Description
===================  =======================================================================
instance_ids         List of instance ids for new instaces
instances            List of instance dicts for new instances (see table below)
tagged_instances     List of instance dicts that already exist if exact_count is used
===================  =======================================================================

EC2 instance dicts
~~~~~~~~~~~~~~~~~~

===================  =======================================================================
Parameter            Description
===================  =======================================================================
id                   instance id
ami_launch_index     instance index within a reservation (between 0 and N-1) if N launched
private_ip           internal IP address (not routable outside of EC2)
private_dns_name     internal DNS name (not routable outside of EC2)
public_ip            public IP address
public_dns_name      public DNS name
state_code           reason code for the state change
architecture         CPU architecture
image_id             AMI
key_name             keypair name
placement            location where the instance was launched
kernel               AKI
ramdisk              ARI
launch_time          time instance was launched
instance_type        instance type
root_device_type     type of root device (ephemeral, EBS)
root_device_name     name of root device
state                state of instance
hypervisor           hypervisor type
===================  =======================================================================

.. _ec2_vpc:

Values returned by ec2_vpc module
---------------------------------

Example output::

    {
      "changed": false,
      "invocation": {
        "module_args": "",
        "module_name": "ec2_vpc"
      },
      "subnets": [
        {
          "az": "us-east-1d",
          "cidr": "10.0.0.0/24",
          "id": "subnet-30d30549",
          "resource_tags": {
            "env": "production",
            "tier": "web"
          }
        },
        {
          "az": "us-east-1d",
          "cidr": "10.0.1.0/24",
          "id": "subnet-43d3054a",
          "resource_tags": {
            "env": "production",
            "tier": "db"
          }
        }
      ],
      "vpc": {
        "cidr_block": "10.0.0.0/16",
        "dhcp_options_id": "dopt-203f5742",
        "id": "vpc-83a135e6",
        "region": "us-east-1",
        "state": "available"
      },
      "vpc_id": "vpc-83a135e6"
    }

===================  =======================================================================
Parameter            Description
===================  =======================================================================
subnets              List of subnet dicts (see below)
vpc                  vpc dict (see below)
vpc_id               vpc id (e.g. `vpc-12345678`)
===================  =======================================================================

subnet dict
~~~~~~~~~~~

===================  =======================================================================
Parameter            Description
===================  =======================================================================
az                   availability zone (e.g., us-east-1d)
cidr                 subnet in CIDR format (e.g., 10.0.0.0/24)
id                   subnet id (e.g. `subnet-12345678`)
resource_tags        dictionary of resource tags
===================  =======================================================================

vpc dict
~~~~~~~~

===================  =======================================================================
Parameter            Description
===================  =======================================================================
cidr_block           subnet in CIDR format (e.g. 10.0.0.0/16)
dhcp_options_id      e.g. `dopt-12345678`
id                   vpc id (e.g., `vpc-12345678`)
region               ec2 region (e.g., us-east-1)
state                state of vpc (e.g., available)
===================  =======================================================================

.. _hostvars:

hostvars from ec2.py dynamic inventory script
---------------------------------------------

ec2.py defines the following host variables:

=============================  =======================================================================
Variable                       Description
=============================  =======================================================================
ec2__in_monitoring_element
ec2_ami_launch_index
ec2_architecture
ec2_client_token
ec2_dns_name
ec2_ebs_optimized
ec2_eventsSet
ec2_group_name
ec2_hypervisor
ec2_id                         instance id
ec2_image_id
ec2_instance_profile
ec2_instance_type
ec2_ip_address
ec2_item
ec2_kernel
ec2_key_name
ec2_launch_time
ec2_monitored
ec2_monitoring
ec2_monitoring_state
ec2_persistent
ec2_placement
ec2_platform
ec2_previous_state
ec2_previous_state_code
ec2_private_dns_name
ec2_private_ip_address
ec2_public_dns_name
ec2_ramdisk
ec2_reason
ec2_region
ec2_requester_id
ec2_root_device_name
ec2_root_device_type
ec2_security_group_ids
ec2_security_group_names
ec2_spot_instance_request_id
ec2_state
ec2_state_code
ec2_state_reason
ec2_subnet_id
ec2_tag_Name
ec2_tag_env
ec2_virtualization_type
ec2_vpc_id
=============================  =======================================================================

.. _ec2_facts:

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

.. _ec2_ami:

Values returned by ec2_ami module
---------------------------------

===================  =======================================================================
Parameter            Description
===================  =======================================================================
image_id             AMI id
state                state of the image
===================  =======================================================================

.. _ec2_vol:

Values returned by ec2_vol module
---------------------------------

===================  =======================================================================
Parameter            Description
===================  =======================================================================
volume_id            volume id
device               device name
===================  =======================================================================

.. _ec2_key:

Values returned by ec2_key module
---------------------------------

===================  =======================================================================
Parameter            Description
===================  =======================================================================
key.fingerprint      SSH public key fingerprint
key.name             SSH keypair name
key.private_key      SSH private key string (only if creating new key)
===================  =======================================================================
