
- cassandra
	- 1m writes/second on GCP https://news.ycombinator.com/item?id=7437493
	- https://news.ycombinator.com/item?id=3529476
		- One of the first Cassandra decisions was dropping vector clocks, reasoning that vector clocks weren't worth the additional complexity for 99% of uses (once you move from key/value to rows + columns). DynamoDB also switched to items/fields and dropped vector clocks (or at least does not expose them).
		- Composite keys (multi-dimensional) and distributed counters were not in the Dynamo paper. They were added to Cassandra, which is indeed based partially on Dynamo.
		- Cassandra initial team was lead by Avinash Lakshman who was one of the authors of Amazon's Dynamo. So it's not strange that Cassandra is hugely inspired by Dynamo (and vice versa).
		- Yes, but the Dynamo paper offers two operations Get(key) and Set(key, value). Anything Cassandra adds atop that they did themselves i.e. column families, secondary indices.
- mongodb
	- my fave talk by mark porter
		- https://www.youtube.com/watch?v=PgCgIz0WYvU&t=885s