Role Name
=========

An Ansible role that installs Postfix with basic configuration on Debian based systems.

Requirements
------------

None

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):
```yaml
postfix_config_file: /etc/postfix/main.cf
```
Location of the Postfix configuration file to be modified.

```yaml
postfix_service_state: started
postfix_service_enabled: true
```
The state in which the Postfix service should be after this role runs, and whether to enable the service on startup.

```yaml
postfix_inet_interfaces: all
postfix_inet_protocols: all
postfix_disable_vrfy_command: yes
postfix_smtpd_tls_loglevel: 1
postfix_smtp_tls_loglevel: 1
postfix_smtpd_tls_security_level: may
postfix_smtp_tls_security_level: may
postfix_message_size_limit: 20480000
```
These correspond to Postfix configuration parameters but are prefixed with `postfix_`.

```yaml
postfix_config_extra: []
```
Allows including additional configuration. See the syntax of `postfix_config`.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - klemens-st.postfix

License
-------

BSD

Author Information
------------------

This role was created in 2025 by Klemens Starybrat.
