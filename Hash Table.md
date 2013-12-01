CS 61B L21: Hash Tables

##Hash Table to store English Words in Dictionary

###Hash Table

    n: actual number of keys (words) stored.
    Table of N buckets. N a bit larger than n.
    A hash table maps huge set of possible keys
    into N buckets by applying a compression 
    function to each hash code.
    h(hashCode) = hashCode mod N   => 0...N-1 (hashCode alywas negative)
    
    Collision: serveral keys hash to same bucket,
    if h(hashCode1) = h(hashCode2）
    
    *Chaining:* each bucket references a linked list of entries, called a chain.
    
    Store each key in table with definition
    entry = (key, value) // key: word; value: definition of that word
    
    
###Operations

    public Entry insert(key, value)
    - compute the key's hash code
    - compress it to determine bucket
    - insert the entry into the bucket's chain
    
    public Entry find(key)
    - hash teh key
    - search chain for entry with given key
    - if found, return it; otherwise null
    
    public Entry remove(key)
    - hash the key
    - search the chain
    - remove from chain if found
    - return entry or null
    
***
### 2 entries with same key, 2 approaches: (a word have two definitions)

    1. G & T: insert both; find() arbitrarily returns one (enumerate all the definitions)
    2. replaced old value with new, only one entry has given key
    
a reference into hashcode, game board => do not change the hash code

### Load factor of a hash table: n/N

    if load function stays low, and hash code & compression function are "good",
    ans no duplicate keys, then the chains are short, & each operation takes 
    constant time O(1).
    
    If load factor get BIG (n >> N), ø(n) time (worse case)
    
    
### Hash Codes & Compression Functions

    key -> hashcode -> [0,N-1]
    
    Ideal: Map each key to a random bucket
    
### Bad compression functions:

    suppose keys are ints,
    hashCode(i) = i.
    compression fn h(hashCode) = hashCode mod N.
    N  = 10,000 buckets
    
    Suppose keys are divisible by 4
    h() is divisible by 4 
    => 
    three quarters of buckets are never used!
    
    Same compression fn better if N is prime.
    
    Better:
    h(hashCode) = ((a*hashCode + b) mod p) mode N
    a, b, p : positive integers
    p is large prime
    p >> N
    mod p => scrabling bits
    
    Now, N(buckets) dosen't need to be prime.
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
