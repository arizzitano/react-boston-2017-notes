# You Might Need Redux (and its ecosystem)
Mark Erikson

## History
- Abramov: you might NOT need redux
- Capabilities via addons etc.
- The best API is often no API
- Make it easy to jump OFF Redux when something better comes around
- [The Tao of Redux](http://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-1/)
- Keep core skinny, enable functionality via addons

## API
- Higher order reducers: similar to HOCs, extend bits of functionality to particular reducers
- Middleware wraps the dispatcher
- Middleware curries dispatch's action handler
- Store enhancers: enable logging, persistent state, etc
- applyMiddleware and the Redux Devtools ARE store enhancers

## Growth & Trends
- 55-60% of React apps use Redux
- Lots of addons available
- Side effects!!!!
    - redux-saga
    - redux-thunk
    - redux-observable
    - redux-loop
- Data fetching:
    - No consistent trend
    - Everybody doing different things
- Store persistence
    - Possible via addons (redux-persist & redux-storage)
    - Offline apps
- Redux routing(??!?)

## Redux Ecosystem
- combining reducers
    - combine-section-reducers
    - combined-reduction
    - ***** topologically-combine-reducers
- composition
    - redux-xforms
    - horux
    - redux-data-structures
- actions
    - redux-actions
- handling data
    - normalizr (write to json)
    - reselect: composable memoized selector functions
    - there are many alternative selector libs
- we should probably be using immutable
    - there are many helper libs available too
- redux-orm: relational data within redux store
- redux-vcr: user tracking?
