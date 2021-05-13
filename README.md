# ansible-elasticsearch
ORTSOC Infra Role: Elasticsearch

All elasticsearch host must disable all swap files

## Variables

* `es_cluster_name`: Name of the Elasticseach cluster
* `elastic_cert_chain`: SSL cert from cert authority, which includes key and cert in p12 format.
* `elastic_http_cert`: HTTPS cert from cert authority in p12 format

Additionally, each Elasticsearch host needs a `master_eligible=[bool]` in the inventory file
