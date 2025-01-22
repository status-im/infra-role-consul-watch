# Consul Service

Create the configuration file for a [Consul](https://www.consul.io/) watch definition.

# Usage

## In Role

```yaml
- name: Create Consul watch definition
  include_role: name=infra-role-consul-watch
  vars:
    consul_watch_name: 'app-abc'
    consul_watches:
      - type: 'services'
        args:
          - "/usr/bin/sudo"
          - "-u"
          - "root"
          - "-g"
          - "root"
          - "/var/lib/python_script.py"
```

The following variables are also available:

* `service_id`
* `handler`
