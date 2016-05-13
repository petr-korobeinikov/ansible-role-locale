ansible-role-locale
===================

Locale generation and configuration.

Requirements
------------

None.

Role Variables
--------------

* `locale_names` is a list of locale names to generate
* `locale_env_vars` is a list of environment variables stored in `/etc/default/locale`.

Dependencies
------------

None.

Example Playbook
----------------

    ---
    - hosts: localhost
      become: true
      roles:
        - role: ansible-role-locale
          locale_names:
            - en_US.UTF-8
            - ru_RU.UTF-8
          locale_env_vars:
            - LC_ALL=ru_RU.UTF-8
            - LANG=ru_RU.UTF-8

License
-------

BSD, MIT
