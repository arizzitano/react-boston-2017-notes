# GraphQL: The Mental Model
Dhaivat Pandya

## Problem: getting data from server to client
- No contract for shape between client and server
- Client doesn't know what kind of data it's going to get back
- Jagged boundary between server and client

## Solution: GraphQL schema
- App data graph
- Relationships between entities = edges in the graph
- GraphQL lets us pick trees out of the graph
- RootQuery -> entity -> fields
- Each query tells us exactly what's being fetched
- With REST, all we have is a URL, no data about what's being fetched
- [Apollo Client](https://github.com/apollographql/apollo-client)

## Caching
- Cache result trees for each query
- Update queries associated with objects in the cache
- Ensure UI consistency
- Identify when we're fetching the same object again
    - Query path contains information about what was previously fetched (e.g. ids)
    - Seems like the only real data required to write to the cache are the distinct identifiers for entities
    - Same ID -> same object
- Assumptions:
    - Same path, same object
    - Same ID, same object
- Indexing?
- Migration path from REST?
