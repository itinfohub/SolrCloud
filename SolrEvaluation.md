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

| Category | Setting |
| --- | --- |
| Solr Version | 8.9.0 |
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
