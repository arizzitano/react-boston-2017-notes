# React + Charts, With and Without Libraries
Christina Holland

## Which browser drawing API?
- HTML
- SVG
- canvas
- webgl

## Library options
- High-level:
    - Most of these wrap D3
    - Highcharts
    - Flot
    - Victory
    - C3
    - Recharts
- Low-level:
    - D3

## HTML
- You might not need all the API of D3
- If it's just rectangles, you can just use divs
- Perf isn't great

## SVG
- each item is a node, so React can diff accordingly
- nice syntax
- accessible-ish
- but this creates lots of elements and is bad for performance :(

## Canvas
- Bitmap/raster
- Stored as pixels, not as individual entities
- Hard to do interactive stuff
- Nothing recognized by React, draw commands are imperative

## WebGL
- v low level, hard to work with
- 3d stuff
- you can draw anything you can imagine
- best performance
- overkill for most use cases

## Using Libraries
- Doesn't work great with React
- Can do chart stuff on top of Flot though
- One-way flow: charting library doesn't always pass state back up
- How to work around this?
    - globals (bad)
    - trigger an event within the browser
- easy axes
- fast
- tested

## Working with React
- Charting library does all the drawing, React doesn't know about it
- React does all the drawing, use libraries for all the math stuff
- React-based libraries (fast, reliable, etc)
