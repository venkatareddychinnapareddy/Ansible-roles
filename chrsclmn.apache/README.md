# Ansible Role: Apache

[![Build Status](https://travis-ci.org/chrsclmn/ansible-role-apache.svg?branch=master)](https://travis-ci.org/chrsclmn/ansible-role-apache)

An Ansible role that installs Apache on Ubuntu 16.04.

## Role Variables

    apache_conf_available: []
    apache_conf_disabled: []
    apache_conf_enabled: []
    apache_mods_disabled: []
    apache_mods_enabled: []
    apache_sites_available: []
    apache_sites_disabled: []
    apache_sites_enabled: []

## Example Playbook

    - hosts: webservers
      vars:
        apache_sites_available:
          - src: mysite.conf
        apache_sites_enabled:
          - mysite
        apache_sites_disabled:
          - 000-default
      roles:
         - { role: chrsclmn.apache }

## License

BSD
