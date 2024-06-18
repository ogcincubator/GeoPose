---
title: GeoPose Basic-YPR (Schema)

language_tabs:
  - json: JSON
  - jsonld: JSON-LD
  - turtle: RDF/Turtle

toc_footers:
  - Version 0.1
  - <a href='#'>GeoPose Basic-YPR</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: GeoPose Basic-YPR (Schema)
---


# GeoPose Basic-YPR `ogc.geo.geopose.basic.ypr`

Basic GeoPose using yaw, pitch, and roll to specify orientation

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="warning">
Validation for this building block has <strong><a href="https://github.com/ogcincubator/GeoPose/blob/main/bblocks/build/tests/geo/geopose/basic/ypr/" target="_blank">failed</a></strong>
</aside>

# Description

GeoPose 1.0 is an OGC Implementation Standard for exchanging the location and orientation of real or virtual geometric
objects (“Poses”) within reference frames anchored to the earth’s surface (“Geo”) or within other astronomical
coordinate systems.

The Basic-YPR Target has a simple structure with no options. Position is specified as a point in an LTP-ENU frame and
rotation is specified by yaw, pitch, and roll angles specified in decimal degrees.

The Basic_YPR.position attribute shall represent the outer frame, specified by an implicit WGS-84 CRS and an implicit
EPSG 4461-CS (LTP-ENU) coordinate system and explicit parameters to define the tangent point.

The Basic_YPR.angles attribute shall represent the inner frame, which is a rotation-only transformation with Yaw, Pitch,
and Roll (YPR) angles, which expressed as three consecutive rotations of a reference frame oriented East-North-Up (ENU)
coordinate system (where the coordinate axes East, North, and Up correspond to the axes X, Y, Z) about the local (
rotated) axes z, y, and x, applied in that order, corresponding to the conventional Yaw, Pitch, and Roll angles. The
unit of measure SHALL be the degree and the angles represented as signed real number values.
# Examples

## Example 1



```json
{
  "position": {
    "lat": 47.7,
    "lon": -122.3,
    "h": 11.5
  },
  "angles": {
    "yaw": 5.514456741060452,
    "pitch": -0.43610515937237904,
    "roll": 0.0
  }
}

```

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_1_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Ftests%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fexample_1_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




```jsonld
{
  "position": {
    "lat": 47.7,
    "lon": -122.3,
    "h": 11.5
  },
  "angles": {
    "yaw": 5.514456741060452,
    "pitch": -0.43610515937237904,
    "roll": 0.0
  },
  "@context": "https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld"
}
```

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_1_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Ftests%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fexample_1_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




```turtle
@prefix geo1: <http://www.w3.org/2003/01/geo/wgs84_pos#> .
@prefix geopose: <http://example.com/geopose/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

[] geopose:angles [ geopose:pitch -4.361052e-01 ;
            geopose:roll 0e+00 ;
            geopose:yaw 5.514457e+00 ] ;
    geopose:position [ geopose:h 1.15e+01 ;
            geo1:lat 4.77e+01 ;
            geo1:long -1.223e+02 ] .


```

<blockquote class="lang-specific turtle">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_1_1.ttl">Open in new window</a>
</blockquote>



## Example 2



```json
{
  "position": {
    "lat": 47.7,
    "lon": -122.3,
    "h": 11.5
  },
  "angles": {
    "yaw": 5.518671098486835,
    "pitch": -0.4381464123477409,
    "roll": 0.0
  }
}

```

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_2_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Ftests%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fexample_2_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




```jsonld
{
  "position": {
    "lat": 47.7,
    "lon": -122.3,
    "h": 11.5
  },
  "angles": {
    "yaw": 5.518671098486835,
    "pitch": -0.4381464123477409,
    "roll": 0.0
  },
  "@context": "https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld"
}
```

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_2_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Ftests%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fexample_2_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




```turtle
@prefix geo1: <http://www.w3.org/2003/01/geo/wgs84_pos#> .
@prefix geopose: <http://example.com/geopose/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

[] geopose:angles [ geopose:pitch -4.381464e-01 ;
            geopose:roll 0e+00 ;
            geopose:yaw 5.518671e+00 ] ;
    geopose:position [ geopose:h 1.15e+01 ;
            geo1:lat 4.77e+01 ;
            geo1:long -1.223e+02 ] .


```

<blockquote class="lang-specific turtle">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_2_1.ttl">Open in new window</a>
</blockquote>



## Example 3



```json
{
  "position": {
    "lat": 47.7,
    "lon": -122.3,
    "h": 11.5
  },
  "angles": {
    "yaw": 5.522894747595089,
    "pitch": -0.4401787262476278,
    "roll": 0.0
  }
}

```

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_3_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Ftests%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fexample_3_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




```jsonld
{
  "position": {
    "lat": 47.7,
    "lon": -122.3,
    "h": 11.5
  },
  "angles": {
    "yaw": 5.522894747595089,
    "pitch": -0.4401787262476278,
    "roll": 0.0
  },
  "@context": "https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld"
}
```

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_3_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Ftests%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fexample_3_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




```turtle
@prefix geo1: <http://www.w3.org/2003/01/geo/wgs84_pos#> .
@prefix geopose: <http://example.com/geopose/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

[] geopose:angles [ geopose:pitch -4.401787e-01 ;
            geopose:roll 0e+00 ;
            geopose:yaw 5.522895e+00 ] ;
    geopose:position [ geopose:h 1.15e+01 ;
            geo1:lat 4.77e+01 ;
            geo1:long -1.223e+02 ] .


```

<blockquote class="lang-specific turtle">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_3_1.ttl">Open in new window</a>
</blockquote>



## Example 4



```json
{
  "position": {
    "lat": 47.7,
    "lon": -122.3,
    "h": 11.5
  },
  "angles": {
    "yaw": 5.527127708845192,
    "pitch": -0.44220204512692407,
    "roll": 0.0
  }
}

```

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_4_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Ftests%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fexample_4_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




```jsonld
{
  "position": {
    "lat": 47.7,
    "lon": -122.3,
    "h": 11.5
  },
  "angles": {
    "yaw": 5.527127708845192,
    "pitch": -0.44220204512692407,
    "roll": 0.0
  },
  "@context": "https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld"
}
```

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_4_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Ftests%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fexample_4_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




```turtle
@prefix geo1: <http://www.w3.org/2003/01/geo/wgs84_pos#> .
@prefix geopose: <http://example.com/geopose/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

[] geopose:angles [ geopose:pitch -4.42202e-01 ;
            geopose:roll 0e+00 ;
            geopose:yaw 5.527128e+00 ] ;
    geopose:position [ geopose:h 1.15e+01 ;
            geo1:lat 4.77e+01 ;
            geo1:long -1.223e+02 ] .


```

<blockquote class="lang-specific turtle">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/GeoPose/bblocks/build/tests/geo/geopose/basic/ypr/example_4_1.ttl">Open in new window</a>
</blockquote>



# JSON Schema

```yaml--schema
allOf:
- $ref: https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/schema.yaml
x-jsonld-extra-terms:
  position:
    x-jsonld-id: http://example.com/geopose/position
    x-jsonld-context:
      lat: http://www.w3.org/2003/01/geo/wgs84_pos#lat
      lon: http://www.w3.org/2003/01/geo/wgs84_pos#long
      h: http://example.com/geopose/h
  angles:
    x-jsonld-id: http://example.com/geopose/angles
    x-jsonld-context:
      yaw: http://example.com/geopose/yaw
      pitch: http://example.com/geopose/pitch
      roll: http://example.com/geopose/roll
x-jsonld-prefixes:
  geopose: http://example.com/geopose/
  geo: http://www.w3.org/2003/01/geo/wgs84_pos#

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Fannotated%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/schema.yaml" target="_blank">https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/schema.json" target="_blank">https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/schema.json</a>


# JSON-LD Context

```json--ldContext
{
  "@context": {
    "position": {
      "@id": "geopose:position",
      "@context": {
        "lat": "geo:lat",
        "lon": "geo:long",
        "h": "geopose:h"
      }
    },
    "angles": {
      "@id": "geopose:angles",
      "@context": {
        "yaw": "geopose:yaw",
        "pitch": "geopose:pitch",
        "roll": "geopose:roll"
      }
    },
    "geopose": "http://example.com/geopose/",
    "geo": "http://www.w3.org/2003/01/geo/wgs84_pos#",
    "@version": 1.1
  }
}
```

> <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2FGeoPose%2Fbblocks%2Fbuild%2Fannotated%2Fgeo%2Fgeopose%2Fbasic%2Fypr%2Fcontext.jsonld">View on JSON-LD Playground</a>

You can find the full JSON-LD context here:
<a href="https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld" target="_blank">https://ogcincubator.github.io/GeoPose/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld</a>

# References

* [OGC GeoPose 1.0 Data Exchange Draft Standard](https://docs.ogc.org/dis/21-056r10/21-056r10.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/GeoPose" target="_blank">https://github.com/ogcincubator/GeoPose</a>
* Path:
<code><a href="https://github.com/ogcincubator/GeoPose/blob/HEAD/bblocks/_sources/basic/ypr" target="_blank">bblocks/_sources/basic/ypr</a></code>

