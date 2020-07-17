# understanding_distributed_systems
`If you can possibly do it without distributed systems then you should do it` - Robert Morris


# What is distributed Systems?
Co-operating computers communication over a network to get some concurrent task done 

### Examples
- Big Data computations like map reduce
- peer to peer file sharing


# Why is it important to learn about it ?
 - critical infrastracture out is basded on distributed
 - At a certain point in time, you will have no choice
 
## But Why ?
 - high performace/ to archieve some form of parellism
 - To tolerate fault 
 -  Some problems are natuarlly spread out in space- Bank transfer across countries
 - Security Goal to archieve isolation
 
# Why is it generally considerd hard?
- Concurrency problems
- Unexpected failure patterns/ Like partial failures
- Often to get performance but it is still tricky and need to more carefull


# Why any developer will be interested?
- Generally for the Developer distributed systerms have interesting problems and solutions which interesting
- Goood a mental model or all the systems we interact on a daily basics

# But before we continue what is a system ?
A software system generally can broken down to three things
 - storage
 - computation
 - communication

So a distributed software system is simply providing useful abstractions around stroage, computation and communication
across multiple computers focused on a specific goal




 
 # Common Topics
 ## Rpc
 - Rpc(mask that we communicating over unreliable networks) (tools)
 
 ## Threads
 - Threads(harness multiple core computers, structure concurrent applications that simplifies a programmers view) (tools)
 
 ## Concurrency Control
 - Concurrency control(An obvious extension of using thread ) (tools)
 
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
 
# Case studies
## MapReduce Framework 
Easy way to run giant distributed computations without worrying developers.

Jobs
Map task
Reduce task

Map Reduce Implementation to count words in some db
```
Map(k,v):
  split v into words
  for each word in words:
    emit(word, 1)
 ```
    
 ```
Reduce(k,v):
   emit(len(v))
```
Nb. Input and reducer output is from GFS(Google FileSystem)


## Is a cluster file system ?
what the hell is that ?



[Robert Morris MIT](https://www.youtube.com/watch?v=cQP8WApzIQQ)
[Simple Note on Distributed Systems](http://book.mixu.net/distsys/single-page.html)

