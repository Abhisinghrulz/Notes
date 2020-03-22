<h1>Cache</h1>

**What is Cache/Caching**

Load balancing helps you scale horizontally across an ever-increasing number of servers, but caching will enable you to make vastly better use of the resources you already have, as well as making otherwise unattainable product requirements feasible.

Caching works on locality of reference principle, recently requested data is likely to be requested again]

It is a short term memory which has limited space but is faster and contains most recently accessed items.

* Cahce can almost be used in every layer : hardware, OS, Web browsers, web application, but are often found nearest to the front end.

**Cache Types**
* Application Server Cache
* Distributed Cache
* Global Cache
* CDN

Application Server Cache
* Placing cache on request layer node enables local storage
* But when you have load balancer, it can send request to any node which can increase **cache miss**
* Two choice to overcome: Distributed Cache & Global Cache

Distributed Cache
* Each of its node own part of cached data
* The cache is divided up using a consistent hashing function, such that if a request node is looking for a certain piece of data, it can quickly know where to look within distributed cache to check if data is available.
* Easily we can increase the cache space just by adding notes to the request pool

Global Cache
* All nodes use the same single cache space
* There can two type of global cache:
    - First, when a cached response not found in cache, cache itself becomes responsible for retrieving the missing piece of data.
    - Second, its the responsibility of request nodes to retrieve any data that is not found
    
CDN
* Its Content Distribution Network for serving large amount of static media which is common to all.
* First request ask the CDN for data, if not, cdn will query the back end servers & then cache it locally.

     
Cache Invalidation -> When cache show 100$ but now sale is for 90$ then we need to invalidate cache and reload
* When data is modified in the DB, it should be invalidated in the cache
* Types
    - Write Through Cache
        * Data is written into the cache and DB at the same time4
        * This minimizes the risk of the data loss, but has the disadvantage of higher latency for write operations
        
    - Write Around Cache 
        * Data is written directly to storage, by passing the cache
        * This reduces flooded write operations but has disadvantage that a read request for recently written data 
          will create a cache miss and must be read from slower back end.
     
    - Write Back Cache
        * Data is written to cache alone & completion is immediately confirm to client and write to permanent storage is done 
          after specified intervals.
        * Risk of Data loss in case of crash.
        
                  
Cache Eviction Policies -> Suppose my cache is full and i want to evict some cache
* FIFO
* LIFO
* LRU (Least Recently Used) -> Best Cache Evict Policy
    - Implement using Doubly Linked List & a hash function containing the reference of node in list
* Most Recently Used
* Least Frequently Used
* Random Replacement