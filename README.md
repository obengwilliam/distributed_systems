# understanding_distributed_systems
`If you can possible do without distributed systems you should do it`
By why
high performance through parellism
tolerate fault 
Natural physical reasons - talking too banks at different locations
Security Goal 


Problems
- Concurreny problems
- Multiple pieces plus a network so many failure problems
- Often to get performance but it is tricky to do it

We will talk about Systems that provide / Abstractions
 - storage
 - Communication
 - Computation

- Abstractions
 Rpc
 Threads
 Concurrency control
 
 # Common Topics
 ## Performance
  - Scalability - cheaper
  
 ## Fault tolerance
  -  There is definitely going to fail if there are over 1000 servers
  What does it mean to be falt ... 
   - Availability - replicate so if one fail, the other one is still active
   - Recoverability - After repair everything should continue to work without nay loss of correctness
   - Non Volatile Storage
   - Replication(make sure the two servers dont drift out of each other)
 
 ## Consistency
 `strong consistency`
  - Key value pair example
  - Making sure things are replicated consistently
  
  ?  sometimes it good to provide week consistent
 
 strong is an expensive consistency
  
  
  throuput
 

## Some case studies to loook
- Peer to peer 
- MapReduce

 
# MapReduce Framework 
Easy way to run giant distributed computations without worrying developers.

Jobs
Map task
Reduce task

Map Reduce Implementation to count words in some db

Map(k,v):
  split v into words
  for each word in words:
    emit(word, 1)
    
Reduce(k,v):
   emit(len(v))


