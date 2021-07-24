# Comparative Study of Solr Performance

The objective is to compare performance of Solr when it is deployed to different running environments such as
physical server, virtual machines, and containers. 

**Solr:** 

   - 8.8.2
   - at the time of writing, a docker image of 8.8.2 is the most recent available version
   - deployed to a physical server, a virtual machine and containers with NAT/host networks

**Performance studied:**
   - indexing 
   - query

**Datasets used:**
  - 6 millions MARC records from the University of Alberta Library (UAL)
  - Education and Research Archive (ERA) of the UAL's institutional repository
  

    
 # Settings
 
**Physical Server**

  | Category | Details |
  |---|---|
  | Memory | 82GB |
  | CPU    | 24 (2x6x2)   |
  | Operating Systems | CentOS 7 |
  | Kernel | 3.10.0-957.el7.x86_64 |
  | Virtualization | VT-x as shown by the command lscpu|
  | Model|Intel(R) Xeon(R) CPU E5645 @2.40GHz|
 
 **KVM Host for Virtual Machines**
 - the same as the above

 **Host of Docker Containers**
 - the same as the physical server

 **SolrCloud**
 - three separate zookeeper hosts (virtual machines on VMWare)
 - three solr nodes (physical servers)
 
