# ansible-elasticsearch
ORTSOC Infra Role: Elasticsearch

All elasticsearch host must disable all swap files

## Variables

* `es_cluster_name`: Name of the Elasticseach cluster
* `elastic_cert_chain`: SSL cert from cert authority, which includes key and cert in p12 format.
* `elastic_http_cert`: HTTPS cert from cert authority in p12 format
* `es_creds`: Dictionary of creds to configure

Additionally, each Elasticsearch host needs a `master_eligible=[bool]` in the inventory file

Example of `es_creds`:
```yml
es_creds:
  - bootstrap: hunter2
  - elastic: hunter2
  - apm_system: hunter2
  - kibana: hunter2
  - kibana_system: hunter2
  - logstash_system: hunter2
  - beats_system: hunter2
  - remote_monitoring_user: hunter2
```