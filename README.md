# rsmt

A library to obtain Rectilinear Steiner Minimal Trees.

For more info on the problem that this solves, check [Rectilinear Steiner tree](https://en.wikipedia.org/wiki/Rectilinear_Steiner_tree). This library implements a fast algorithm that provides exact (ie: minimal) solutions.

**NOTE**: The library is still under development.

## Usage

To use it, just do:

```js
import rsmt from `rsmt`

const nodes = [[0, 0], [1, 2], [4, 1], ...]
const solution = await rsmt(nodes)

/*
solution = {
  terminals: [[0, 0], [1, 2], [4, 1], ...],
  steiners: [[0, 1], ...],
  edges: [[[0, 0], [0, 1]], ...],
  edgeIds: [[1, -1], ...]
}
*/
```

## Acknowledgements

This library is a reimplementation of the algorithms used in [GeoSteiner](http://www.geosteiner.com/), based on the paper "*A New Exact Algorithm for Rectilinear Steiner Trees*" (David M. Warme, 1997).

We also make use of an emscripten build of glpk, named [glpk.js](https://github.com/jvail/glpk.js/).