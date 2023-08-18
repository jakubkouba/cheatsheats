# Ruby

## Installation
:bomb: `cannot load such file -- openssl (LoadError)` Old version of ruby (2.7 and less) use old version of openssl. 

:wrench: Pass the openssl lib path explicitely with option `$ rvm install --with-openssl-dir=/usr/local/opt/openssl@1.1` (You need to have openssl@.1.1 instlled => `$ brew install openssl@1.1`) 


## Optimisation

- Most od the performance problems with ruby is with memory and Garbage Collection. To reduce this issues we need to thin how ruby programs use a memory

The memory usage of the process can be obtained from RSS (Residen Set Size). It's the portion of memory that the process helds in RAM. It's in bytes
`$ ps -o rss -p {pid}`

in Ruby: `puts "%dM" % \`ps -o rss= -p #{Process.pid}\ `.to_i`

:point_right: Don't use ruby for large data processing. Use rather worker which will use other external tool

:point_right: Always ask how much memory the code consumes. In ruby all is an object. Using ruby build in iterators might look nice, but it can consume lots of memory

:point_right: Look at the algorithm as a last think. The memory is most odf the time the problem

### Memory usage optimisation
- MALLOC_ARENA_MAX env var affects how ruby uses the memory allocation. Values 1 or 2 can brin a good results. [RubyConf 2019 - Parallel Ruby: Managing the Memory Monster by Kevin Miller](https://www.youtube.com/watch?v=4_yxbh9Enoc&t=1227s)   
