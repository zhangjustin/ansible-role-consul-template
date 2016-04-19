Ansible Role: Consul-Template
=========

Install Consul-Template on CentOS servers.

Requirements
------------

Written in Ansible 2.0.*

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

## consul_template_enabled

Enable consul-template or not.

Default is `true`.

## consul_template_supervisor_enabled

Install consul-template in supervisor or not.

Default is `true`.

## consul_template_user

User for consul-template.

Default user is `consul`.

## consul_template_group

Group for consul-template.

Default group is `consul`.

## consul_template_version

Version of consul-template.

Default version is `0.10.0`.

## consul_template_release

Release name of consul-template.

Default is `consul-template_0.10.0_linux_386`.

## consul_template_archive_file

Release archive file name of consul-template.

Default is `consul-template_0.10.0_linux_386.tar.gz`.

## consul_template_download_url

Download URL.

Default is `https://github.com/hashicorp/consul-template/releases/download/v0.10.0/consul-template_0.10.0_linux_386.tar.gz`.

## consul_template_home

Home directory for consul-template.

Default is `/home/consul/consul-template`

## consul_template_config_file_template

Template name for consul-template main fragment.

Default is `consul-template.cfg.j2`.

Note: this template will generate `{{ consul_template_home }}/config/fragments/1_main.cfg`.

## consul_template_config_file

Consul-template config file name.

Default is `consul-template.cfg`.

Note: this will be generated under `{{ consul_template_home }}/config`.

## consul_template_consul_server

Consul server for consul-template to connect.

Default is `127.0.0.1`.

Dependencies
------------

+ juwai.supervisor, when consul_template_supervisor_enabled

Example Playbook
----------------

    - hosts: servers
      roles:
        - juwai.consul-template

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2016 by [Juwai Limited](http://www.juwai.com).
