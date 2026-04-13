# Note 32

## Caches

### Four important questions

* Where do I put a new cache block in the cache?
* How can I tell if a cache block is already in the cache?
* Which cache block should I replace?
* What happens on writes?

### Organizations

Block address = byte address / block size (integer division)
Number of blocks = cache size / block size

* Direct-mapped cache
  * Index = block address % number of blocks
  * Tag   = block address / number of blocks
* Fully-associative cache
  * Index = N/A
  * Tag   = block address
* N-way set-associative cache
  * Index = (block address % number of blocks) / n
  * Tag   = block address / (number of block / n)

### Replacement policies

* Random
* Least recently used (LRU)

### Write policies

On a cache hit:
* Write-through
* Write-back

On a cache miss:
* Write-allocate
* No-write-allocate

Typical:
* Write-through + no-write-allocate
* Write-back + write-allocate
