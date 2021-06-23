# Deploy Solr and SolrCloud

This is to document how to deploy Solr/SolrCloud on a CentOS 7 host.

The Solr version is 8.9.0. 

# Preparation of the Host Machines

#### Host Machine Resources
  
  | Category | Details |
  |---|---|
  | Memory | 32GB |
  | CPU    | 8    |
  | Operating Systems | CentOS 7 |
  | Kernel | 3.10.0-957.el7.x86_64 |
  | Virtualization | VT-x as shown by the command 'lscpu | grep -i virtualization'|
