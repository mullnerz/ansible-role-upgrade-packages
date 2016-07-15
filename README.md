ansible-role-upgrade-packages
=========

This role upgrades system packages and initiates a reboot if it is required and configured.

Requirements
------------

No special requirements, but note that this role requires root access, so either run it in a playbook with a global `become: yes`, or invoke the role in your playbook like:

    - hosts: servers
      roles:
        - role: ansible-role-upgrade-packages
          become: yes

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    reboot_if_required: false

Dependencies
------------

None.

Example Playbook
----------------

Upgrade system packages without a reboot by default:

    - hosts: servers
      become: yes
      roles:
        - ansible-role-upgrade-packages

Upgrade system packages with a reboot if it is required:

    ansible-playbook test.yml -e reboot_if_required=true

License
-------

BSD

Author Information
------------------

This role was created in 2016 by [Zoltán Müllner](http://zoltan.mullner.hu/).
