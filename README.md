# ansible-role-elrepo

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-elrepo.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-elrepo)

RHEL/CentOS - ELRepo Project

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    elrepo_dist: "{{ ansible_distribution_major_version }}"
    elrepo_disablerepo: []
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

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
