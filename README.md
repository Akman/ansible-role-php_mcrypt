# Ansible Role: php_mcrypt

Installs mCrypt package for php on Linux.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    php_mcrypt_user: root
    php_mcrypt_group: root

    mcrypt_version: '1.0.1'
    # mcrypt_version: '1.0.0'

    php_mcrypt_config_filename: "mcrypt.ini"

    php_extension_conf_paths:
      - "/etc/php/{{ php_version }}/fpm/conf.d"
      - "/etc/php/{{ php_version }}/apache2/conf.d"
      - "/etc/php/{{ php_version }}/cli/conf.d"

## Dependencies

  - geerlingguy.php

## Example Playbook

    - hosts: all
      roles:
        - akman.php_mcrypt

*Inside `vars/main.yml`*:

    mcrypt_version: '1.0.1'
    # mcrypt_version: '1.0.0'

## License

MIT / BSD

## Author Information

This role was created in 2018 by Alexander Kapitman
