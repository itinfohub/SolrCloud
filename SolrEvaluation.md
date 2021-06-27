# Overview

This document presents a comparative study of the performance of Solr while deployed on 
a physical server, a virtual machine and a container. 

This study is also augmented to Azure cloud to deploy a solr instance as an IaaS, Paas, and
a Container service. The performance in the cloud is compared with the performance on-premise.
The cost of running Solr as IaaS, PaaS, and a Container service in the Azure cloud is also 
presented and analyzed.

This might be instrumental to people who are working in libraries for their adoption of 
cloud computing. 

# Common Settings

>```
>Container 8.8.2: openjdk version "11.0.11" 2021-04-20
>OpenJDK Runtime Environment 18.9 (build 11.0.11+9)
>OpenJDK 64-Bit Server VM 18.9 (build 11.0.11+9, mixed mode, sharing)
>```

| Category | Setting |
| --- | --- |
| Solr Version | 8.8.2 |
| Jetty Version | |
| Max Heap Memory | 8192MB |
| Min Heap Memory | 8192MB |
| EBSCO UADATA    | 6211347 Docs|

 
# On-premises Solr Deployment

The physical machine is a dedicated Supermicro machine with the following settings:

#### CPU Characteristics

| Computing Resource Category | Setting |            
|---|---|
| Processor Model | Intel(R) Xeon(R) E5645 |        
| Processor Clock   | 2.40GHz |                     
| Sockets           | 2 |                           
| Cores per Socket  | 6 |                            
| Threads per Core  | 2 |                          
| Total CPUs        | 24 |                          
| Total Memory      | 90,567,040 kB |              


#### Storage Media Specification

  | Storage Media Property | Value |
  | --- | --- |
  | Storage Media Type |  3.5 Inch HDD |
  | Make | Seagate |
  | Model |  Constellation ES.3 |
  | Capacity | 1TB |
  | Cache Size | 128 MB |
  | Rotaional Speed | 7200 RPM |
  | Bandwidth | SATA 6Gb/s | 
  
#### Performance (EBSCO UADATA 6,211,347 Docs)

| Experiment  | Test 1 (seconds)  | Test 2 (seconds) | Test 3 (seconds)| Average (seconds) |
|---|---|---|---|---|
|Physical Server |5275|5323 |5353 |
|VM |6070 | 6055 |6138 |
|Container|5554 |5523 | 5521 |

# Network Bandwidth and Latency Evaluation Tools

The tools are employed to measure network bandwidth and latency, which are useful for
performance comparison.

1. [qperf](https://access.redhat.com/solutions/21226811)

# References

1. Yadav A.K., Garg M.L., Ritika (2019) Docker Containers Versus Virtual Machine-Based Virtualization. In: Abraham A., Dutta P., Mandal J., Bhattacharya A., Dutta S. (eds) Emerging Technologies in Data Mining and Information Security. Advances in Intelligent Systems and Computing, vol 814. Springer, Singapore. https://doi.org/10.1007/978-981-13-1501-5_12
2. Wes Felter, Alexandre Ferreira, Ram Rajamony, Juan Rubio (2015). [An Updated Performance Comparison of Virtual Machines and Linux Containers](https://ieeexplore-ieee-org.login.ezproxy.library.ualberta.ca/stamp/stamp.jsp?tp=&arnumber=7095802). IEEE international symposium on performance analysis of systems and software (ISPASS). pp: 171-172
3. Sogand Shirinbab, Lars Lundberg & Emiliano Casalicchio. (2020). Performance evaluation of containers and virtual machines when running Cassandra workload concurrently.
```
To cite:
 Shirinbab S, Lundberg L, Casalicchio E. Performance evaluation of containers and virtual machines when running
Cassandra workload concurrently. Concurrency Computat Pract Exper. 2020;e5693. https://doi.org/10.1002/cpe.5693

```


# Datasets

1. [database dump](http://www.informatics.jax.org/downloads/database_backups/)
2. EBSCO MARC Records
