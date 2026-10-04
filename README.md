# Shrink

This is a small web 3D platformer game (it has exactly 3KiB, 3072 bytes!) made for the [Shrink Hack Club event](https://shrink.hackclub.com).

## How to use it

Copy the contents of [dist/uri.txt](dist/uri.txt) and paste them into the browser's address bar. If it's too hard, or you just want to explore the map, run `player.y = 100` in the browser console.

## How it works

The code from [src/index.html](src/index.html) is minified using [build.mjs](build.mjs) into [dist/uri.txt](dist/uri.txt).

The minifier from the [Shrink guide](https://shrink.hackclub.com/app/guides/setup) was modified to shorten HTML tag attributes and add a newline after the `#version 300 es` shader directive.

This game uses WebGL 2. Every cube is drawn using 36 vertices (6 faces × 2 triangles per face × 3 vertices per triangle). The shader also takes the camera settings as uniforms for every cube. The platformer physics are simple because the map is grid-based.

There are two versions of the source code: [src/index.orig.html](src/index.orig.html) contains the full, non-manually-minified code, while [src/index.html](src/index.html) contains a manually minified, less readable version with GL constants replaced, shortened shader variable names, etc. to fit exactly 3072 bytes.

## Building

```sh
npm install
node build.mjs
```
