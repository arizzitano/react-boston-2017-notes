# Get that CSS out of your JS!
Brian Hough

## Why CSS in JS?
- Portability of components
- Portability of styles
- Better handling of critical CSS
- Platform agnostic styling

## How to share styles?
- cut and paste
- require specific build

## Problems
- Reuse of styles
- How to share between components
- OOCSS, SMACSS, BEM
- Solution: hashed styles as classnames

## Style vs component portability
- csslock
- mixins become regular functions, portable everywhere

## Critical CSS
- required to do a first render of a page
- inline it (??!?) to improve render times
- pretty manual
- requires build tools
- tool called critical tries to automate this

## Styles for every platform
- react primitives (recyclable across platforms)
- CSS-like API vs smaller library
- emotion: CSS-like API, small size, fast performance

## Stuff to read
- http://bit.ly/css-js-security
- http://bit.ly/css-escape
- http://bit.ly/js-styles-perf
- http://bit.ly/unified-styling-language
- CSS variables
