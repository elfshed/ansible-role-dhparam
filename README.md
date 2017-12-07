shored.dhparam
==============

This role is used to write a file containing pre-generated dhparams. The dhparms are from Mozilla's wiki
at https://wiki.mozilla.org/Security/Server_Side_TLS#Pre-defined_DHE_groups

Requirements
------------

None.

Role Variables
--------------

`dhparam_size`

Size of the dhparam to use. Supported values: 2048, 3072, 4096. Default is 4096.

`dhparam_file`

Location to output the dhparms to. Default location is `/etc/ssl/dhparam.pem`.

Dependencies
------------

None

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: shored.dhparams, dhparam_size: 2048, dhparam_file: /etc/ssl/dhparam.pem }

License
-------

BSD

Author Information
------------------

Edward Shornock <edward.shornock@elfgroup.fi>
