# ansible-elasticsearch
ORTSOC Infra Role: Elasticsearch

All elasticsearch host must disable all swap files

## Variables

* `es_cluster_name`: Name of the Elasticseach cluster

Additionally, each Elasticsearch host needs a `master_eligible=[bool]` in the inventory file
