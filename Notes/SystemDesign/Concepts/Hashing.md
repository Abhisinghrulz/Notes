<h1>HASHING</h1>

Purpose of Hashing
* Hashing is used to index data
* In Cryptographic application
* Sharding the keys
* Finding duplicate Records

Hashing
- Hashing is generating a value or values from 
    a string of text using a mathematical function called Hash Function.
- Hashing is one way to enable security during the process of message transmission 
    when the message is intended for a particular recipient only 
    
Hash Function
- Division Method -> num % 10
- Midsquare method -> 3214 -> square -> 103|29|796
                        Take 29
- Folding Method -> 45|31|16 -> 31


What is a good Hash Function?
- Easy to compute
 - Even distribution
 - Less collision
 
 
<b>How to resolve collision (Simple collision handling):</b>


 - We can have sepearate chaining when more than 1 item is in cell. New item will be at the front. 
 - By this way we can insert all items, but searching & deletion will take time. 
 - This is open hashing as we'll creating linked list to add collision.
 
 
**Open addressing (Closed hashing)**
 - In this, data goes inside the table, no need to make linked list
 **- By linear probing**
  - If x mod 10 is already present, do on (x + 1) mod 10, if it's present too, do on (x + 2) mod 10
  - Issue is there'll block of data in chucks, not evenly distributed
 **- For it, quadratic probing**
  - In this H(x) = (Hash(x) + f(i))
  - f(i) = i ^ 2;
 **- Double Hashing**
  - f(i) = i * Hash2(x)
  - Hash2(x) = R - x mode R (i.e R = 7)
