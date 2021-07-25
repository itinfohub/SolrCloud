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

**Containers**
 - container with NAT
 - container with network=host

 **SolrCloud**
 - three separate zookeeper hosts (virtual machines on VMWare)
 - three solr nodes (physical servers)
 
# Datasets

### MARC records at UAL

- MARC is an acrynonym for Machine Readable Cataloging.
- At UAL, we currently have over 6 million records
- The ingest application is SolrMarc.jar, a free and Open Source Software (FOSS)

### ERA 
- ERA is a short for Education and Research Archive at UAL
- It is an institutional respository (IR) for the University of Alberta.
- It encompasses theses, research articles, teaching materials and many others.
- The indexing of through Ruby and Rails application with a customized rake task
- There are about 63K records.

# Experiments

### Ingestings

Measure the elapsed time for ingesting ERA and MARC records to servers deployed to different
running forms. The same type of ingests is repeated three times, the average is taken from
the three measurements. The heap memory of the corresponding machine is set to be 8092MB for
all the cases across the board. 

| Server | ERA  | MARC UAL |
|---|---|---|
| Physical|Y|Y|
| VM|Y|Y|
| Container(NAT)|Y|Y|
| Container(HOST)|Y|Y|
| Solrcloud|Y|Y|

### Queries

The query logs from our production were taken, and used as test queries for five different servers.


| Server | ERA  | MARC UAL |
|---|---|---|
| Physical|Y|Y|
| VM|Y|Y|
| Container(NAT)|Y|Y|
| Container(HOST)|Y|Y|
| Solrcloud|Y|Y|

### Profiling heap memory usage




