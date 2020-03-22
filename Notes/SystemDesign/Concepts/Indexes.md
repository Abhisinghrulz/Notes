<h1>INDEXES</h1>

* Useful in database to improve the speed of data retreival.
* Index makes trade-off of increased storage overhead, slower writes for the benefit of faster read.
* Index is a data structure of table of contents that points us to the location where actual data lives, so when we create 
    an index on a column of a table, we store that column & a pointer to the whole row in the index.
    
Types of Indexing
* Ordered Indexing
    - Column is sorted as per ascending order.
* Hash Indexing
    - Indexing is as per Hash function & Hash Table