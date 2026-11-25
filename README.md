# Clover georeference test

A live example of [Clover](https://clover.iiif.library.northwestern.edu)'s `<clover-viewer>` web component opening an AnnotationPage as its content: a georeference that lays Hokusai's _The Great Wave off Kanagawa_ (an Understory Manifest) over Edo Bay, and a GeoJSON point on Mount Fuji.

- Page: [`index.html`](index.html), live at https://mathewjordan.github.io/clover-georeference-test/
- Annotations: [`assets/annotations/test-annotations.json`](assets/annotations/test-annotations.json), an AnnotationPage of two:
  - "View from Edo Bay", a `georeferencing` annotation on the whole Canvas, its four corners pinned to open water out in the bay off Kanagawa (Yokohama)
  - "Mount Fuji", the mountain's region tagged with a GeoJSON point at its summit (IIIF Cookbook recipe 0139)

Each annotation names its Manifest in `partOf`, so Clover opens it. A `georeferencing` annotation given through the `annotations` attribute beside a Manifest is left out (Clover 4.12.3), so the AnnotationPage is the `iiif-content`, by its full address.

```html
<script src="https://cdn.jsdelivr.net/npm/@nulib/clover/dist/web-components/index.umd.js"></script>

<clover-viewer
  iiif-content="https://mathewjordan.github.io/clover-georeference-test/assets/annotations/test-annotations.json"
  template="default"
  items="grid"
  header="false"
>
</clover-viewer>
```
