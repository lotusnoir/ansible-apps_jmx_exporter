# Ansible Role: ansible-apps_jmx_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_graylog_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_graylog_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_graylog_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_graylog_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_graylog_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_graylog_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_graylog_exporter.svg)](https://github.com/lotusnoir/ansible-apps_graylog_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_graylog_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_graylog_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_graylog_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_graylog_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_graylog_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_graylog_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_graylog_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_graylog_exporter)

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

## Prometheus rules

TODO

## Grafana dashboard

A sample dashboard is available here: [https://grafana.com/grafana/dashboards/13571](https://grafana.com/grafana/dashboards/135)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
