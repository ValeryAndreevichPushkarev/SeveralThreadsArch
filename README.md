# SeveralThreadsArch
This repository contains a simple CPU with Several pipelines that work with single ALU (that lead us to Zero Stall CPU, because of cache misses)

## Simplified description
Any access to memory on any architecture is limited to the speed of light. 
So if we have several threads (with registers, part of the stack, execution pipelines) that work with one ALU, we can get almost zero penalties on Cache Miss.
If we get L3 cache miss, we can simply continue to execute any pending thread that will probably have data in cache.
If the possibility of cache miss is 10%, that for 2 threads we have 1% chance of stalling execution block.
For 4 threads and 1 ALU, we get almost 0.01%.

So making a cache miss callback or even FIFO with threads makes a great sense.

Especially when you have arithmetic cores with about 200 transistors switching on FO-4 and 6 GHz.
And almost can't use any caches because of that.

TODO:

Send greatings to Rakes Kumar, NTNU xD
