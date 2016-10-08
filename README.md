nvm
===

Install nvm and Node.js.

Requirements
------------

git, curl, build-essential, libssl-dev. Requirements are installed by the role.

Role Variables
--------------

* `nvm.user` Remote user. Defaults to ansible `remote_user`.
* `nvm.version` nvm version tag, or `HEAD`. Defaults to `v0.4.0`
* `nvm.node_version` Node.js version. Defaults to `'0.10.'`
* `nvm.packages` list of package node. Defaults to `'[]'`

Dependencies
------------

No depedencies.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: nvm
          nvm:
            user: deploy
            version: v0.17.3
            node_version: '0.10'
            packages:
              - bower
              - karma

License
-------

BSD

Author Information
------------------

Jarno Keskikangas
