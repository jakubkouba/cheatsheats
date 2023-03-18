# Ruby

## Optimisation

- Most od the performance problems with ruby is with memory and Garbage Collection. To reduce this issues we need to thin how ruby programs use a memory

The memory usage of the process can be obtained from RSS (Residen Set Size). It's the portion of memory that the process helds in RAM. It's in bytes
`$ ps -o rss -p {pid}`

in Ruby: `puts "%dM" % \`ps -o rss= -p #{Process.pid}\`.to_i`
