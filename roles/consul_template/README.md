Consul-Template
=========

Installs consul-template as either an SystemD service.

Example Playbook Role Usage
----------------

## Simple setup

Install and run consul-template using Upstart with a barebones config file that contains no template configuration.

```yml
roles:
    - { role: consul-template }
```

## Use your own config file

Provide your own configuration file for consul-template.

```yml
roles:
    - { role: consul-template,
        consul_template_config_file_template: "{{ playbook_dir }}/files/consul-template.cfg.j2"
    }
```

