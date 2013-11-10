Quick reference
===============

Quick reference to parameters and special variables.

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
---------------

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
environment
with_items          List of items to iterate over
with_nested         List of list of items to iterate over in nested fashion
with_fileglob       List of local files to iterate over, described using shell fileglob notation
                    (e.g., ``/playbooks/files/fooapp/*``)
with_first_found
with_together       Dictionary of lists to iterate over in parallel
with_random_choice  List of items to be selected from at random
until               Boolean, task will retry until evaluates true or until ``retries``
retries             Used with "until", number of times to retry. Default: ``3``
delay               Used with "until", seconds to wait between retries. Default: ``10``

==================  =========================================================================================


Host variables that modify ansible behavior
-------------------------------------------

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
----------------------------

=================              ==================================================                  =====================================================================================================================================================================================================================================================
Parameter                      Description                                                         Example
=================              ==================================================                  =====================================================================================================================================================================================================================================================
ansible_date_time              Dictionary that contains date info                                  ``{"date": "2013-10-02", "day": "02", "epoch": "1380756810", "hour": "19","iso8601": "2013-10-02T23:33:30Z","iso8601_micro": "2013-10-02T23:33:30.036070Z","minute": "33","month": "10","second": "30","time": "19:33:30","tz": "EDT","year": "2013"}``
=================              ==================================================                  =====================================================================================================================================================================================================================================================

