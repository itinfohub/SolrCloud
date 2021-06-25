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


# Solr/SolrCloud Performance

1. [Five Ways to Optimize Sitecore Solr Search Performance](https://www.searchstax.com/blog/5-ways-to-optimize-your-solr-search-performance-for-sitecore/)
2. [Apache Solr Memory Tuning for Production](https://blog.cloudera.com/apache-solr-memory-tuning-for-production/)
3. [Configure Solr for Optimum Performance](https://medium.com/tech-tajawal/tips-and-tricks-to-maximize-apache-solr-performance-74e8ea4f5c8d)
4. [Improving Solr Performance](https://tech.olx.com/improving-solr-performance-f4202d28b72d)



# Solr Replication, Backup and Restore

1. [API for Solr Replication, Backup and Restore](https://solr.apache.org/guide/6_6/making-and-restoring-backups.html)
