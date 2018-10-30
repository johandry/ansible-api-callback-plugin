Role Name
=========

This is an Ansible role to build a Go program, it was made for testing the Ansible callback plugin project.

All the code to build is located in the `files/` directory. It will be moved to `$GOPATH/src/` and the binary, result of the compilation, is located in the root (`/`) directory.

Requirements
------------

It requires Go to be installed in the system. This could be done with the Ansible role `go/install`.

Role Variables
--------------

This role accepts the following variables:

- `bin_name`: name of the binary to build
- `owner`: username of the program owner, it's usually the GitHub username.

Dependencies
------------

Depends of the `go/install` Ansible role.

Example Playbook
----------------

This is a simple example of how to use the role using variables passed in as parameters:

    - hosts: servers
      roles:
         - { role: go/build, bin_name: service }

License
-------

MIT

Author Information
------------------

Open an issue in this repository to fix or include any feature, however this role is just for testing, it does not require to be perfect and using Ansible to build a Go code is not an optimal thing to do.
