troykinsella.go
===============

An ansible role for installing the go language from binary archive.

Dependencies
------------

* troykinsella.archive

Role Variables
--------------

* `go_version`: Optional. The version of go to install. Default: `1.8.1`.
* `go_archive_os`: Optional. The target operating system. Default: `linux`.
* `go_archive_architecture`: Optional. The target system architecture. Default: `amd64`.
* `go_archive_file_name`: Optional. The name of the archive file to download. Default: `go{{ go_version }}.{{ go_archive_os }}-{{ go_archive_architecture }}.tar.gz`.
* `go_archive_base_url`: Optional. The installation archive base URL. Default: `https://storage.googleapis.com/golang/`.
* `go_archive_checksum`: Optional. The expected installation archive checksum. Default: `a579ab19d5237e263254f1eac5352efcf1d70b9dacadb6d6bb12b0911ede8994`.
* `go_archive_checksum_algorithm`: Optional. The installation archive checksum algorithm. Default: `sha256`.
* `go_archive_cache_path`: Optional. The directory path into which the archive will be downloaded. Default: `/usr/local/pkg`.
* `go_archive_destination_path`: Optional. The installation prefix directory path. Default: `/usr/local`.
* `go_archive_extracted_file_name`: Optional. The expected name of the root file or directory that is extracted from the archive. Default: `go`.
* `go_archive_destination_file_name`: Optional. Rename the extracted directory to this value. Default: `go{{ go_version }}`.
* `go_archive_destination_link_name`: Optional. Create a symbolic link having this name to the `go_archive_extracted_file_name` (or `go_archive_destination_file_name`, when specified). Default: `go`.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: troykinsella.go
          go_version: 1.8.1
          go_archive_checksum: a579ab19d5237e263254f1eac5352efcf1d70b9dacadb6d6bb12b0911ede8994

License
-------

MIT
