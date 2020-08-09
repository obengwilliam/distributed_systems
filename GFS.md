# Big Storage
 - simple storage system
 reasonably well behaved system
 
 why hard ?
 aggregate performance - >split data from huge number of servers - sharding .. const faults
 -> fault tolerance then it leads to -> replication -> inconsistency
 ->consistency-> low performance
 
 
# Google File System
Big
Fast  - High Parellel Access
Global / Universal resuable storage system
Sharding
Automatic failure recovery

Non Goals
Designed to work in one signle data centers
Internal User
Big Sequential Access

Not consistence with read
Get away with single master
 -  Applications should be accompanied with checksum on record boundaries
 
 
 

it reflected real workd expeirence of implement

- Master Data


Questions ?
 - How did they use checksums to accomodate for inconsistent reads?
 - what is a chunk server ?
 - What is the master server ?
 
 
 


