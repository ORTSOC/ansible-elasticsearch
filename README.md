ansible-elasticsearch
=========

Deploys search, a log indexer and search tool.

Requirements
------------

- Debian 10
- sudo
- ssh

Role Variables
--------------

- `es_cluster_name`: Name of the Elasticseach cluster
- `elastic_cert_chain`: SSL cert from cert authority, which includes key and cert in p12 format.
- `elastic_http_cert`: HTTPS cert from cert authority in p12 format

Inventory Host Variables
----------------

- `master_eligible=[bool]`: Required. determines whether this given host can be declared as a master elastic node.

Example Playbook
----------------

```yaml
es_cluster_name: ortsoc
```

Example Inventory File
---------

```
[elasticsearch]
es1.my.domain master_eligible=true
es2.my.domain master_eligible=true
es3.my.domain master_eligible=true
es4.my.domain master_eligible=false
es5.my.domain master_eligible=false
```

License
-------

GPL3

Author Information
------------------

ORTSOC, Oregon State University
