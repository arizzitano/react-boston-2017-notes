# Lightning Talks

## Layout Animations
Vincent Riemer
- FLIP: first, last, invert, play
- take desired first measurements & last measurements of the shape
- diff them and apply difference as transform
- play the transform
- LayoutAnimation
- ResizeObserver: observe changes to content rect
- There is no position observer
- This is mostly POC
- https://git.io/layoutanim

## React Native: The Good Parts
Stan Bershadskiy
- React Native Cookbook
- React <-> Bridge <-> Native UI SDK
- BETTER THAN Cordova, Ionic, etc jank
- Layout system, yoga
- Native module bridge gives you access to OS's native functions
- 50% of commits coming from the community (!!!! how can we do this?)
- upgrading is rly hard, you have to follow along with the breaking changes
- Apps much slower in development mode
- create-react-native-app

## Bringing your Snapshot Tests to Life
Carly Litchfield
- Snapshot testing compares output of tests to make sure it hasn't changed over time
- With react it's a rendered component
- The good:
    - it's really simple to implement
    - jest --updatesnapshot does automatic updates
- The bad:
    - diffs are painful!!!!!
- Filling the gaps:
    - Percy: does an image comparison (visual reviews) https://percy.io
    - seems pretty nice tbh
    - can test at different screen sizes
- Integrating into codebase
    - works well with storybook!!!! <3
    - stories become percy snapshot tests

## How to Spin a Good Yarn Package
Kaylie Alexa Kwon
- Yarn STILL faster than NPM 5
- yarn upgrade-interactive -- nicer than npm, runs inline
- save frequently used flags
- customize config (opt out of deps, scripts, etc) - good for perf
- debugging easily
- yarn why
- resolve nested dependencies (resolutions field)
