# Ansible Role: ssh server

Run ssh server and manage ssh keys

[![Build Status](https://travis-ci.org/AlphaNodes/ansible-ssh.svg?branch=master)](https://travis-ci.org/AlphaNodes/ansible-ssh)

## Dependencies

  none

## Example Playbook with just ssh server

    - hosts: localhost
      roles:
        - AlphaNodes.ssh

## Example Playbook with key management

    - hosts: localhost
      vars:
        ssh_users
          - name: root
            access:
              - company_user1.pub
              - company_user2.pub
            with_management_access: no
            keys:
              - host: github.com
                user: git
                dir: company1
                source_dir: company1_company2
          - name: user3
            access:
              - company_user3.pub -->
      roles:
        - AlphaNodes.ssh

## License

GPL Version 3

## Author Information

This role was created in 2019 by [AlphaNodes](https://alphanodes.com/).
