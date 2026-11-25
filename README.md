# Clover georeference test

A live example of [Clover](https://clover.iiif.library.northwestern.edu)'s `<clover-viewer>` web component showing a place on a map from an annotation added beside an Understory Manifest of Hokusai's _The Great Wave off Kanagawa_.

- Page: [`index.html`](index.html), live at https://mathewjordan.github.io/clover-georeference-test/
- Annotations: [`assets/annotations/test-annotations.json`](assets/annotations/test-annotations.json), an AnnotationPage that tags Mount Fuji's region of the print with a GeoJSON point at its summit (IIIF Cookbook recipe 0139)

```html
<script src="https://cdn.jsdelivr.net/npm/@nulib/clover/dist/web-components/index.umd.js"></script>

<clover-viewer
  iiif-content="https://iiif-understory.dc.library.northwestern.edu/published/presentation/manifest/12e964fd-532c-4c17-8f09-da8ec9d3bbe1/manifest.json"
  template="default"
  items="grid"
  header="false"
  annotations="assets/annotations/test-annotations.json"
>
</clover-viewer>
```
