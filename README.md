# Ansible Role: ansible-apps_jmx_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_jmx_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_jmx_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__jmx_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_jmx_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_jmx_exporter/tags)

Deploy [jmx_exporter](https://github.com/prometheus/jmx_exporter/) to expose jmx metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `jmx_exporter_version` | 0.14.0 | jmx_exporter version |
| `jmx_exporter_install_method` | deb | install binmary from deb file |
| `jmx_exporter_install_dir` | /etc/jmx_exporter | config files directory |
| `jmx_exporter_config_files` | [] | config files |
| `jmx_exporter_address` | 0.0.0.0 | jmx_exporter listen address |
| `jmx_exporter_port` | 9117 | jmx_exporter listen port |

## Examples

	---
	- hosts: apps_jmx_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_jmx_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
