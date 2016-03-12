troykinsella.go
===============

An ansible role for installing the go language from binary archive

Dependencies
------------

* troykinsella.archive

Role Variables
--------------

* go_version: Optional. The version of go to install. Default: 1.6
* go_archive_os: Optional. The target operating system. Default: linux
* go_archive_architecture: Optional. The target system architecture. Default: amd64
* go_archive_base_url: Optional. The installation archive base URL. Default: https://storage.googleapis.com/golang/
* go_archive_checksum: Optional. The expected installation archive checksum. Default: 5470eac05d273c74ff8bac7bef5bad0b5abbd1c4052efbdbc8db45332e836b0b
* go_archive_checksum_algorithm: Optional. The installation archive checksum algorithm. Default: sha256
* go_archive_cache_path: Optional. The directory path into which the archive will be downloaded. Default: /usr/local/pkg
* go_archive_destination_path: Optional. The installation prefix directory path. Default: /usr/local
* go_archive_extracted_file_name: Optional. The expected name of the root file or directory that is extracted from the archive. Default: go
* go_archive_destination_file_name: Optional. Rename the extracted directory to this value.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: troykinsella.go
          go_version: 6
          go_archive_os: linux
          go_archive_architecture: amd64
          go_archive_checksum: 5470eac05d273c74ff8bac7bef5bad0b5abbd1c4052efbdbc8db45332e836b0b
          go_archive_destination_path: /usr/local

License
-------

MIT
