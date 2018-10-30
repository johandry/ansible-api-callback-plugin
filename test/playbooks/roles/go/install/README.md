Role Name
=========

This is an Ansible role to install Go. This is a sample role to test the Ansible callback plugin but still can be used to install Go.

Requirements
------------

This role just require Ansible to be installed.

Role Variables
--------------

This role uses the following variables:

- `go_version`
- `go_tarball_checksum`

To get their values go to [Go Downloads](https://golang.org/dl/) and identify the latest Go version number, for example `1.11.1`, and assign this number to the variable `go_version`.

Then expand that version to locate the `linux-amd64.tar.gz` link, get (copy and paste) the SHA256 checksum and assign this value to the `go_tarball_checksum` variable but adding the prefix `sha256:`. Example: `"sha256:2871270d8ff0c8c69f161aaae42f9f28739855ff5c5204752a8d92a1c9f63993"`

Dependencies
------------

This role does not have any dependency but it's a dependency for other roles in this project.

Example Playbook
----------------

This is a simple example of how to use the role using variables passed in as parameters:

    - hosts: localhost
      roles:
         - { role: go, go_version: 1.11.2, go_tarball_checksum: "sha256:2871270d8ff0c8c69f161aaae42f9f28739855ff5c5204752a8d92a1c9f63993" }

License
-------

MIT

Author Information
------------------

This role is a copy from [ansible-go](https://github.com/jlund/ansible-go) with some minor modifications.
