---
title: GeoPose Basic-Quaternion (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>GeoPose Basic-Quaternion</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: GeoPose Basic-Quaternion (Schema)
---


# GeoPose Basic-Quaternion `ogc.geo.geopose.basic.quaternion`

Basic GeoPose using quaternion to specify orientation

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong>valid</strong>
</aside>


# JSON Schema

```yaml--schema
description: 'Basic-Quaternion: Basic GeoPose using quaternion to specify orientation'
definitions:
  Position:
    type: object
    properties:
      lat:
        type: number
      lon:
        type: number
      h:
        type: number
    required:
    - lat
    - lon
    - h
  Quaternion:
    type: object
    properties:
      x:
        type: number
      y:
        type: number
      z:
        type: number
      w:
        type: number
    required:
    - x
    - y
    - z
    - w
type: object
properties:
  position:
    $ref: '#/definitions/Position'
    x-jsonld-id: http://example.com/geopose/position
  quaternion:
    $ref: '#/definitions/Quaternion'
    x-jsonld-id: http://example.com/geopose/quaternion
required:
- position
- quaternion
x-jsonld-prefixes:
  geopose: http://example.com/geopose/
  geo: http://www.w3.org/2003/01/geo/wgs84_pos#

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbblocks%2Fbuild%2Fannotated%2Fgeo%2Fgeopose%2Fbasic%2Fquaternion%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/quaternion/schema.yaml" target="_blank">https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/quaternion/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/quaternion/schema.json" target="_blank">https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/quaternion/schema.json</a>


# JSON-LD Context

```json--ldContext
{
  "@context": {
    "position": "geopose:position",
    "quaternion": "geopose:quaternion",
    "geopose": "http://example.com/geopose/",
    "geo": "http://www.w3.org/2003/01/geo/wgs84_pos#",
    "@version": 1.1
  }
}
```

> <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbblocks%2Fbuild%2Fannotated%2Fgeo%2Fgeopose%2Fbasic%2Fquaternion%2Fcontext.jsonld">View on JSON-LD Playground</a>

You can find the full JSON-LD context here:
<a href="https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/quaternion/context.jsonld" target="_blank">https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/quaternion/context.jsonld</a>

# References

* [OGC GeoPose 1.0 Data Exchange Draft Standard](https://docs.ogc.org/dis/21-056r10/21-056r10.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/GeoPose" target="_blank">https://github.com/ogcincubator/GeoPose</a>
* Path:
<code><a href="https://github.com/ogcincubator/GeoPose/blob/HEAD/bblocks/_sources/basic/quaternion" target="_blank">bblocks/_sources/basic/quaternion</a></code>
