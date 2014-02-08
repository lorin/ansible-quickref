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
