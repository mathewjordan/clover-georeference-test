# Clover georeference test

A live example of [Clover](https://clover.iiif.library.northwestern.edu)'s `<clover-viewer>` web component opening a Manifest with an AnnotationPage sideloaded through `annotations`: a georeference that lays Hokusai's _The Great Wave off Kanagawa_ (an Understory Manifest) over Edo Bay, and a GeoJSON point on Mount Fuji.

- Page: [`index.html`](index.html), live at https://mathewjordan.github.io/clover-georeference-test/
- Annotations: [`assets/annotations/test-annotations.json`](assets/annotations/test-annotations.json), an AnnotationPage of two:
  - "View from Edo Bay", a `georeferencing` annotation on the whole Canvas, its four corners pinned to open water out in the bay off Kanagawa (Yokohama)
  - "Mount Fuji", the mountain's region tagged with a GeoJSON point at its summit (IIIF Cookbook recipe 0139)

Clover lays each annotation on the Canvas it targets, as if the Manifest held it. A `georeferencing` annotation given through `annotations` needs Clover 4.12.5 or later, so the script is pinned to that release. Each annotation also names its Manifest in `partOf`, so the AnnotationPage still opens on its own as `iiif-content`.

```html
<script src="https://cdn.jsdelivr.net/npm/@nulib/clover@4.12.5/dist/web-components/index.umd.js"></script>

<clover-viewer
  iiif-content="https://iiif-understory.dc.library.northwestern.edu/published/presentation/manifest/12e964fd-532c-4c17-8f09-da8ec9d3bbe1/manifest.json"
  annotations="assets/annotations/test-annotations.json"
  template="default"
  items="grid"
  header="false"
>
</clover-viewer>
```
