# What's New & What's Next for Server Side Rendering

Sasha Aickin, Redfin

## React 16 Stuff
- React 16 is backward compatible (but not cross compatible)
- If no warnings, you can upgrade safely!!!!
- For SSR, render() -> hydrate()
- render() can return arrays and strings! you don't need to nest it in a container element
- Nonstandard attrs will still get passed through
    - I wonder if there's a way to disable this?
- Generates more efficient HTML on the server, not full of garbage comments etc
- Error Boundaries (component can catch errors that happen in its children)
    - Don't work on server
- Portal: rendering child component to different place in the DOM
    - Useful for dialogs etc
    - Was unstable in 15
    - Legit supported in 16
    - Doesn't work in SSR :(
- Less strict with client side hydration
    - Generated markup checksum on the server has to match the checksum on the client
    - If not, React barfs in 15
    - In 16, it walks the DOM and fills in the differences
    - Doesn't check the attrs though (perf change)
- Doesn't neeed to be compiled for SSR
    - process.ENV calls are expensive
    - with 15:
- Performance
    - massively faster on server
    - 74% (just looking at renderer time)
- Can render to a stream (!!!!)
    - renderToNodeStream (similar to renderToString) renders to a readable stream
    - Todo: read up on readable/writable streams in Node
    - HTTP response is a writable stream. You can pipe a stream to an http response
    - Immediate TTFB
    - CPU sharing
    - This allows you to round-robin/multithread responses

## What's Next?
- Asynchronous rendering????
    - Block rendering within an async/await
    - Little confused about the use case here. Seems anti-reactive tbh
    - Only really makes sense for client
    - Big Pipe helps with this
    - Serialization possible drawback. Parent/child nesting triggers this
