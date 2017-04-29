# Ansible Role: Kibana [![Build Status](https://travis-ci.org/jradtilbrook/ansible-role-kibana.svg?branch=master)](https://travis-ci.org/jradtilbrook/ansible-role-kibana)

This role installs and configures Kibana 5.x for the Elastic stack.

It has only been designed to work on Ubuntu 16.04, but other Debian flavours
should also work.


## Requirements

None.


## Role Variables

`kibana_config_settings` is a YAML dictionary used to fully configure Kibana.
The contents of this variable are written the configuration file in YAML
format. Therefore, it accepts any valid configuration property supported by
Kibana.

`kibana_install_state`: This is useful for updating Kibana to newer versions
after it has already been installed. Use `latest` to achieve this functionality.


## Resources

Documentation related to Kibana can be found at the links below:

- [documentation](https://www.elastic.co/guide/en/kibana/current/index.html)


## Dependencies

None, but you may want to run Kibana behind a proxy - I recommend using the
[geerlingguy.nginx](https://github.com/geerlingguy/ansible-role-nginx) role.

Check out my other roles on [Ansible Galaxy](https://galaxy.ansible.com/jradtilbrook)
if you are installing the entire Elastic Stack.


## Example Playbook

```yaml
- hosts: servers
  become: yes

  roles:
    - role: jradtilbrook.kibana
```


## License

MIT
