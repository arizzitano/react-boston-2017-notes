# GraphQL Subscriptions: Full Stack
Robert Zhu

## Primer
- http://graphql.tk
- reads
    - client <-> http server <-> graphql server
    - everything is a POST
- writes aka mutations
    - same lifecycle
    - combines write with read
- queries and mutations
    - SERVER decides shape of resource it returns
    - gives client stuff it doesn't need (overfetching)
    - sometimes it underfetches and you have to make another roundtrip
    - too much junk in memory, too much stuff over the wire
- real time data??
    - subscriptions
    - MAY run into scaling issues (lol)
    - event stream called Response Stream
    - subscription creates persistent function on the server mapping source stream to response stream
    - you can read off the event stream :)
- state scaling is v hard
    - subscribers, documents/variables, etc

## Resources