# ansiblebit.macports

[![License](http://img.shields.io/badge/license-New%20BSD-blue.svg?style=flat)](https://raw.githubusercontent.com/ansiblebit/macports/master/LICENSE)
[![Platforms](http://img.shields.io/badge/platforms-macosx-lightgrey.svg?style=flat)](#)

[![Project Stats](https://www.openhub.net/p/ansiblebit-macports/widgets/project_thin_badge.gif)](https://www.openhub.net/p/ansiblebit-macports/)

An [Ansible](http://www.ansible.com) role for [macports](http://www.macports.org).


## Tests

| Family | Distribution | Version | Test Status |
|:-:|:-:|:-:|:-:|
| Darwin | MacOSX  | 10.10  | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |


## Requirements

- ansible >= 1.9


## Role Variables

### User defined variables

| variable | default value | description |
|:--------:|:-------------:|:------------|
| macports_version | 2.3.4 | the macports version to be installed. |
| macports_upgrade_outdated | yes | flag to determine if outdated ports should be upgraded after the installation process. |
| macports_selfupdate | yes | flag to determine if the latest port revisions should be downloaded. |


### Default variables

| variable | description |
|:--------:|:------------|
| macports_build_from_source | flag to determine if macports is to be installed from source (not supported yet). |
| macports_force_install | flag to indicate if a new install is to be performed even if macports is already present in the server. |
| macports_installer | hash that contains the filename and SHA256 checksum of the macports files for each supported OS family and distribution. |
| macports_tarball | the file name of the macports tarball. |
| macports_tarball_url | the prefix for the URL from which the macports tarball will be downloaded. |


## Dependencies

None.


## Playbooks

    - hosts: servers
      roles:
         - { role: ansiblebit.macports,
             macports_version: 2.3.4,
             macports_selfupdate: yes,
             macports_upgrade_outdated: yes }

## License

BSD

## Author Information

- [steenzout](http://github.com/steenzout)

