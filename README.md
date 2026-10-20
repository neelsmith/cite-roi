# cite-roi

A TypeScript package to work with regions of interest on citable images.

Packages using `cite-roi`:


- [imageviewer](https://github.com/neelsmith/imageviewer)
- [iiif-cite](https://github.com/neelsmith/iiif-cite)


## RoIs

A region of interest (RoI) is represented as a scale-independent expression in the form `{ x, y, w, h }` (top-left corner plus width and height), where are values are in the range `0..1`.  


## Functions

- `screenToFrac` / `roiToScreen`: convert between viewer coordinates and fractions, given a
  view `{ scale, x, y }` (translate + scale applied to the full-resolution image) and the image size
- `roiFromCorners`, `moveRoi`, `resizeRoi`: build and edit regions, kept inside the image
- `formatRoi` / `parseRoi`, `formatRois` / `parseRois`: `x,y,w,h` strings (four decimals), `;`-separated lists
- `roiUrn(imageUrn, roi)`: CITE2 URN with a region extension, e.g.
  `urn:cite2:hmt:vaimg.2017a:VA012RN_0013@0.1000,0.2000,0.3000,0.4000`



## Packaging

The package ships TypeScript source (no build step); consumers bundle it with Vite.

```sh
npm install
npm test
npm run typecheck
```

Install in another project from GitHub:

```sh
npm install github:neelsmith/cite-roi#v1.0.0
```
