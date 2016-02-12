troykinsella.go
===============

An ansible role for installing the go language from binary archive

Dependencies
------------

* troykinsella.archive

Role Variables
--------------

* go_version: The version of go to install
* go_archive_os: The target operating system. Default: linux
* go_archive_architecture: The target system architecture. Default: amd64
* go_archive_base_url: The installation archive base URL. Default: https://storage.googleapis.com/golang/
* go_archive_checksum: The expected installation archive checksum. Default: 43afe0c5017e502630b1aea4d44b8a7f059bf60d7f29dfd58db454d4e4e0ae53
* go_archive_checksum_type: The installation archive checksum algorithm. Default: sha256
* go_archive_destination_path: The installation prefix directory path. Default: /usr/local

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: troykinsella.go
          go_version: 1.5.3
          go_archive_os: linux
          go_archive_architecture: amd64
          go_archive_checksum: 43afe0c5017e502630b1aea4d44b8a7f059bf60d7f29dfd58db454d4e4e0ae53
          go_archive_destination_path: /usr/local

License
-------

MIT
