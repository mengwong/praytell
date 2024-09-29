# MVP User Story

## Publish

Alice talks to her LLM, saying "hey, I'm unexpectedly free this afternoon. Would anybody near me like to grab coffee?"

This gets saved to a database of some sort running in the PrayTell system.

It could be RAG-like vector-store database thing. There are vector databases we can use, like Lance, or Pinecone, etc.

Or we can do an even simpler non-vector DB like Cassandra or Postgresql.

## Subscribe / Query

Bob talks to his LLM, saying "hey, I'm in the mood for coffee this afternoon. Is there anyone nearby who wants to meet up?"

That query runs against the PrayTell system and eventually connects him to Alice.

# Moving Parts: Use Case 1

Alice's LLM and Bob's LLM are running on different providers.

But both of them have "agentic" connectors to PrayTell.

Alice's LLM rewrites her intent ("prayer") into a JSON blob and publishes it into the PrayTell publish API (the "pray" part).

Bob's LLM rewrites his prayer into a JSON blob / SQL query? / NoSQL query? and calls some endpoint.

Later, Bob and Alice manage to meet.
