Open Distro for Elasticsearch
=========

Documentation: https://opendistro.github.io/for-elasticsearch-docs

Build
------------

Master branch:
[![Build Status](https://travis-ci.org/timon2013/ansible-role-opendistro.svg?branch=master)](https://travis-ci.org/timon2013/ansible-role-opendistro)

Dev Branch:
[![Build Status](https://travis-ci.org/timon2013/ansible-role-opendistro.svg?branch=dev)](https://travis-ci.org/timon2013/ansible-role-opendistro)

Requirements
------------

```bash
meta/main.yml
```

Role Variables
--------------

Default variables are in defaults directory.

| Name | Default               | Type          | Description                       |
| ---- | --------------------- | ------------- | ----------------------------------|
| `redhat_packages` | defaults/main.yml     | Array         | Packages for installation         |
| `redhat_services` | elasticsearch.service | Array         | List of services to be launched   |
| `default_security_plugins` | true                  | Bool          | Installing the default configuration of the security plugins |
| `default_es_conf` | true | Bool | Installing the default configuration of the opendistro, only for elasticsearch.yml file. |
| `default_jvm_conf` | true | Bool | Installing the default configuration of the jvm, only for jvm.options file. |
| `opendistro_security_plugin_files` | defaults/main.yml | Array | The security configuration for plugin opendistro_security in yaml format. |
| `security_plugin_passwords`| defaults/main.yml | Array | The login and password for opendistro users. The sequence is important and dependent from opendistro_security_plugin_files configuration. |
| `opendistro_db_dir` | /var/lib/elasticsearch | String | The path to elasticsearch databases directory |
| `opendistro_http_port` | 9200 | Number | The http port for elasticsearch |
| `opendistro_log_dir` | /var/log/elasticsearch | String | The path to log directory |
| `opendistro_elasticsearch_variables` | deafults/main.yml | Array | The configuration for elasticsearch in elasticsearch.yml file. This is yaml format. |
| `opendistro_java_home` | /usr/lib/jvm/java-11 | String | The path to java home direcotry |
| `opendistro_java_variables` | defaults/main.yml | Array | The configuration for jvm in jvm.options file. |
| `opendistro_plugin_dir` | /usr/share/elasticsearch/plugins | String | The path to plugin directory |

Dependencies
------------

None

Example Playbook
----------------

```bash
molecule/default/playbook.yml
```

License
-------

MIT License

Author Information
------------------

timon2013
