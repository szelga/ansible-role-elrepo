# ansible-role-elrepo

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-elrepo.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-elrepo)

RHEL/CentOS - ELRepo Project

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    elrepo_dist: "{{ ansible_distribution_major_version }}"
    elrepo_disable_plugin: []
    elrepo_disablerepo: []
    elrepo_enable_plugin: []
    elrepo_enablerepo: []
    elrepo_kernel: false
    elrepo_kernel_version: lt
    elrepo_packages: []
    elrepo_repository_elrepo: false
    elrepo_repository_extras: false
    elrepo_repository_kernel: false
    elrepo_repository_testing: false

## Dependencies

 * https://galaxy.ansible.com/linuxhq/epel/

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.elrepo
          elrepo_disable_plugin:
            - post-transaction-actions
          elrepo_enablerepo:
            - epel
          elrepo_kernel: true
          elrepo_kernel_version: ml
          elrepo_packages:
            - dkms
            - kmod-r8168
            - redhat-lsb-languages
          elrepo_repository_elrepo: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
