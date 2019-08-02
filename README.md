Logz Filebeat
=============

Role started as a fork from https://github.com/geerlingguy/ansible-role-filebeat

Setup `filebeat` service on a RedHat/Debian/Ubuntu Linux server and configure it to use a Logz.io account via token. 

Requirements
------------

To use the role add these lines to `requirements.yml` file

```yaml
- src: https://github.com/channelweb/ansible-logz-filebeat
  name: logz-filebeat
```

Then with usual `ansible-galaxy install -r requirements.yml` role will be added

Variables
---------

Only mandatory variable is Logz access token `{{ filebeat_logz_token }}` that should be defined in a `vault` file.

Example
-------

To launch role simply include in a playbook roles definition:

```yaml
    - role: logz-filebeat
      become: yes
```

License
-------

BSD

