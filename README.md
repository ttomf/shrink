# Shrink

This is a small web game (under 3KB) made for [Shrink Hackclub event](https://shrink.hackclub.com).

## How to use it

Copy the contents of [dist/uri.txt](dist/uri.txt) and paste them into browser's address bar. If it's too hard or you just want to explore the map, run `player.y = 100` in browser console.

## How it works

The code from [src/index.html](src/index.html) is minified using [build.mjs](build.mjs) to [dist/uri.txt](dist/uri.txt).

The game uses WebGL 2, every cube is drawn using vertex shader applied to 36 points (6 faces * 2 triangles for each face * 3 vertices for each triangle). Shader also takes camera settings as an uniform for every cube. The platformer physics is simple, because the map is in a grid.

## Building

```sh
npm install
node build.mjs
```
