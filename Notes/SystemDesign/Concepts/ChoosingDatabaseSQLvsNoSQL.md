<h1>Choosing Database SQL vs NoSQL</h1>

**What is SQL Database**
* It stores data in row and columns
* MySQL, Oracle, SQLite
* Each record has fixed schema, columns must be decides before data entry, can be altered but involves modifying whole database & going offline.
* It uses SQL Query
* SQL are vertically scalable i.e. by increasing the higher memory, CPU of hardware, which can be very expensive

**What is NoSQL Database**
* Here schemas are dynamic, Columns can be added on the fly and each row doesn't have to contain each columns.
* Here queries are focused on collection of documents, its also known as UNQL( UnStructured Query Language)
* These are horizontally scalable meaning we can add more servers easily. Lots of servers are distributed data servers also.
* Most of NoSQL sacrifice ACID compliance for performance and scalability.
* Cloud based computing and storage. They are designed to be scaled across multiple data servers.

**No-SQL Databases**
* Key-Value Stores : Redis, Voldemart, Dynamo
* Document Database : MongoDB, CouchDB
* Wide-Column Database : 
    - Column families 
    - Best suited for analyzing large dataset 
    - Cassendra, HBase
    
* Graph Database :
    - Data is saved in graph structure with nodes(entities), properties and lines(Connection).
    - Neo4J, InfiniteGraph
    

* When to choose SQL Database
    - When schema not likely to change much
    - when you want to ensure ACID compliance and your data is structured and unchanging.
    
* When to choose NoSQL Database
    - When schemas are dynamic
    - When storing large volume of data with rapid development with no structured fixed
    - When data needs to be stored across servers in different regions.        