# Distributed Queue

A prototype of visualizing N queues and the effect of different enqueuing and
dequeueing algorithms.

I haven't settled on the terminology for this project, but basically the flow
is `creator/owner` inserts a `packet/job` in a `queue` and then a `worker`
processes it eventually removing it.

- packets -> queues
  - random
  - sequential
  - shuffle shard
  - sequential prioritized with rate limiting and demotion
- workers -> queues
  - random
  - sequential
  - shuffle shard
  - sequential prioritized
  - random prioritized
- worker switch opportunities
  - every packet
  - every N packets
  - empty
  - never
- situations
  - single worker slow down
  - all worker slow down
  - flood from one creator
  - flood from all creator
  - one creator large packets



## Reference

[Join-Idle-Queue: A Novel Load Balancing Algorithm for Dynamically Scalable Web Services](http://research.microsoft.com/pubs/153348/idleq.pdf)

[Shuffle Sharding: massive and magical fault isolation](http://www.awsarchitectureblog.com/2014/04/shuffle-sharding.html)
