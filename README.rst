===============
Quick reference
===============

Quick reference to parameters and special variables.

Facts
=====

See facts_.

.. _facts: facts.rst


EC2 stuff
=========

See ec2_.

.. _ec2: ec2.rst

Docker stuff
============

See docker_.

.. _docker: docker.rst

Built-in variables
==================

These are variables that are always defined by ansible.

============================   =========================================================================================================================================================================================================
Parameter                      Description
============================   =========================================================================================================================================================================================================
hostvars                       A dict whose keys are Ansible host names and values are dicts that map variable names to values
group_names                    A list of all groups that the current host is a member of
groups                         A dict whose keys are Ansible group names and values are list of hostnames that are members of the group. Includes ``all`` and ``ungrouped`` groups: ``{"all": [...], "web": [...], "ungrouped": [...]}``
inventory_hostname             Name of the current host as known by ansible.
play_hosts                     A list of inventory hostnames that are active in the current play (or current batch if running serial)
ansible_version                A dict with ansible version info: ``{"full": 1.8.1", "major": 1, "minor": 8, "revision": 1, "string": "1.8.1"}``
role_path                      The current role’s pathname (available only inside a role)
============================   =========================================================================================================================================================================================================

These can be useful if you want to use a variable associated with a different host. For
example, if you are using the EC2 dynamic inventory and have a single host with
the tag "Name=foo", and you want to access the instance id in a different play,
you can do something like this::

    - hosts: tag_Name_foo
      tasks:
        - action: ec2_facts

      ...

    - hosts: localhost
      vars:
        instance_id: {{ hostvars[groups['tag_Name_foo'][0]]['ansible_ec2_instance_id'] }}
      tasks:
        - name: print out the instance id for the foo instance
          debug: msg=instance-id is {{ instance_id }}

Internal variables
==================

These are used internally by Ansible.

============================   =========================================================================================================================================================================================================
Variable                       Description
============================   =========================================================================================================================================================================================================
playbook_dir                   Directory that contains the playbook being executed
inventory_dir                  Directory that contains the inventory
inventory_file                 Host file or script path (?)
============================   =========================================================================================================================================================================================================




Play parameters
---------------

===================  =======================================================================
Parameter            Description
===================  =======================================================================
any_errors_fatal
gather_facts         Specify whether to gather facts or not
handlers             List of handlers
hosts                Hosts in the play (e.g., ``webservers``).
include              Include a playbook defined in another file
max_fail_percentage  When ``serial`` is set on a play, and some hosts fail on a
                     task, if the percentage of hosts that fail exceeds this
                     number, Ansible will fail the whole play. (e.g., ``20``).
name                 Name of the play, displayed when play runs (e.g., ``Deploy a foo``).
pre_tasks            List of tasks to execute before roles.
port                 Remote ssh port to connect to
post_tasks           List of tasks to execute after roles.
remote_user          Alias for ``user``.
role_names
roles                List of roles.
serial               Integer that indicates how many hosts Ansible should manage at a single
su
su_user
become               Boolean that indicates whether ansible should become another user (e.g., ``True``).
become_user          If become'ing,  user to become as. Defaults: ``root``.
sudo                 (deprecated, use become) Boolean that indicates whether ansible should use sudo (e.g., ``True``).
sudo_user            (deprecated, use become_uesr) If sudo'ing,  user to sudo as. Defaults: ``root``.
tasks                List of tasks.
user                 User to ssh as. Default: ``root`` (unless overridden in config file)
no_log
vars                 Dictionary of variables. **this is the holy grail of variables, it will output everything!**
vars_files           List of files that contain dictionary of variables.
vars_prompt          Description of vars that user will be prompted to specify.
vault_password
===================  =======================================================================

Task parameters
===============

==================  =========================================================================================
Parameter           Description
==================  =========================================================================================
name                Name of the task, displayed when task runs (e.g., ``Ensure foo is present``).
action              Name of module to specify. Legacy format, prefer specifying module name directly instead
args                A dictionary of arguments. See docs for ``ec2_tag`` for an example.
include             Name of a separate YAML file that includes additional tasks.
register            Record the result to the specified variable (e.g., ``result``)
delegate_to         Run task on specified host instead.
local_action        Equivalent to: ``delegate_to: 127.0.0.1``.
remote_user         Alias for ``user``.
user                User to ssh as for this task
become              Boolean that indicates whether ansible should become another user (e.g., ``True``).
become_user         If become'ing,  user to become as. Defaults: ``root``.
sudo                Boolean that indicates whether ansible should use sudo on this task
sudo_user           If sudo'ing, user to sudo as.
when                Boolean. Only run task when this evaluates to True. Default: ``True``
ignore_errors       Boolean. If True, ansible will treat task as if it has succeeded even if it returned an
                    error, Default: ``False``
module              More verbose notation for specifying module parameters. See docs for ``ec2`` for an example.
environment         Mapping that contains environment variables to pass
failed_when         Specify criteria for identifying task has failed (e.g., ``"'FAILED' in command_result.stderr"``)
changed_when        Specify criteria for identifying task has changed server state
with_items          List of items to iterate over
with_nested         List of list of items to iterate over in nested fashion
with_fileglob       List of local files to iterate over, described using shell fileglob notation
                    (e.g., ``/playbooks/files/fooapp/*``)
with_first_found    Return the first file or path, in the given list, that exists on the control machine
with_together       Dictionary of lists to iterate over in parallel
with_random_choice  List of items to be selected from at random
with_dict           Loop through the elements of a hash
with_sequence       Loop over a range of integers
until               Boolean, task will retry until evaluates true or until ``retries``
retries             Used with "until", number of times to retry. Default: ``3``
delay               Used with "until", seconds to wait between retries. Default: ``10``
run_once            If true, runs task on only one of the hosts
always_run          If true, runs task even when in --check mode
==================  =========================================================================================

Complex args
============
There are three ways to specify complex arguments:

just pass them::

    - ec2_tag:
        resource: vol-abcdefg
        tags:
          Name: my-volume

action/module parameter::

    - action:
        module: ec2_tag
        resource: vol-abcdefg
        tags:
          Name: my-volume

args parameter::

    - ec2_tag: resource=vol-abcdefg
      args:
        tags:
          Name: my-volume




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

These are the same as the output of Facts described in a previous section.
Currently, this just has one variable defined.

=================              ==================================================                  =====================================================================================================================================================================================================================================================
Parameter                      Description                                                         Example
=================              ==================================================                  =====================================================================================================================================================================================================================================================
ansible_date_time              Dictionary that contains date info                                  ``{"date": "2013-10-02", "day": "02", "epoch": "1380756810", "hour": "19","iso8601": "2013-10-02T23:33:30Z","iso8601_micro": "2013-10-02T23:33:30.036070Z","minute": "33","month": "10","second": "30","time": "19:33:30","tz": "EDT","year": "2013"}``
=================              ==================================================                  =====================================================================================================================================================================================================================================================

Return value of a loop
======================

If you register a variable with a task that has an iteration, e.g.::

    - command: echo {{ item }}
      with_items:
        - foo
        - bar
        - baz
      register: echos

Then the result is a dictionary with the following values:

==========      =============================================================
Field name      Description
==========      =============================================================
changed         boolean, true if anything has changed
msg             a message such as "All items completed"
results         a list that contains the return value for each loop iteration
==========      =============================================================

For example, the ``echos`` variable would have the following value::

    {
        "changed": true,
        "msg": "All items completed",
        "results": [
            {
                "changed": true,
                "cmd": [
                    "echo",
                    "foo"
                ],
                "delta": "0:00:00.002780",
                "end": "2014-06-08 16:57:52.843478",
                "invocation": {
                    "module_args": "echo foo",
                    "module_name": "command"
                },
                "item": "foo",
                "rc": 0,
                "start": "2014-06-08 16:57:52.840698",
                "stderr": "",
                "stdout": "foo"
            },
            {
                "changed": true,
                "cmd": [
                    "echo",
                    "bar"
                ],
                "delta": "0:00:00.002736",
                "end": "2014-06-08 16:57:52.911243",
                "invocation": {
                    "module_args": "echo bar",
                    "module_name": "command"
                },
                "item": "bar",
                "rc": 0,
                "start": "2014-06-08 16:57:52.908507",
                "stderr": "",
                "stdout": "bar"
            },
            {
                "changed": true,
                "cmd": [
                    "echo",
                    "baz"
                ],
                "delta": "0:00:00.003050",
                "end": "2014-06-08 16:57:52.979928",
                "invocation": {
                    "module_args": "echo baz",
                    "module_name": "command"
                },
                "item": "baz",
                "rc": 0,
                "start": "2014-06-08 16:57:52.976878",
                "stderr": "",
                "stdout": "baz"
            }
        ]
    }
