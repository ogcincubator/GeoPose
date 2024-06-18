
# GeoPose Basic-YPR (Schema)

`ogc.geo.geopose.basic.ypr` *v0.1*

Basic GeoPose using yaw, pitch, and roll to specify orientation

[*Status*](http://www.opengis.net/def/status): Under development

## Description

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
## Examples

### Example 1
#### json
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

#### jsonld
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
  "@context": "https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld"
}
```

#### ttl
```ttl
@prefix geopose: <http://example.com/geopose/> .

[] geopose:angles [ ] ;
    geopose:position [ ] .


```


### Example 2
#### json
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

#### jsonld
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
  "@context": "https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld"
}
```

#### ttl
```ttl
@prefix geopose: <http://example.com/geopose/> .

[] geopose:angles [ ] ;
    geopose:position [ ] .


```


### Example 3
#### json
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

#### jsonld
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
  "@context": "https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld"
}
```

#### ttl
```ttl
@prefix geopose: <http://example.com/geopose/> .

[] geopose:angles [ ] ;
    geopose:position [ ] .


```


### Example 4
#### json
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

#### jsonld
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
  "@context": "https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld"
}
```

#### ttl
```ttl
@prefix geopose: <http://example.com/geopose/> .

[] geopose:angles [ ] ;
    geopose:position [ ] .


```

## Schema

```yaml
description: 'Basic-YPR: Basic GeoPose using yaw, pitch, and roll to specify orientation'
definitions:
  angles:
    type: object
    properties:
      yaw:
        type: number
      pitch:
        type: number
      roll:
        type: number
    required:
    - yaw
    - pitch
    - roll
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
type: object
properties:
  position:
    $ref: '#/definitions/Position'
    x-jsonld-id: http://example.com/geopose/position
  angles:
    $ref: '#/definitions/angles'
    x-jsonld-id: http://example.com/geopose/angles
required:
- position
- angles
x-jsonld-prefixes:
  geopose: http://example.com/geopose/
  geo: http://www.w3.org/2003/01/geo/wgs84_pos#

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/ypr/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/ypr/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "position": "geopose:position",
    "angles": "geopose:angles",
    "geopose": "http://example.com/geopose/",
    "geo": "http://www.w3.org/2003/01/geo/wgs84_pos#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcincubator.github.io/GeoPose/bblocks/bblocks/build/annotated/geo/geopose/basic/ypr/context.jsonld)

## Sources

* [OGC GeoPose 1.0 Data Exchange Draft Standard](https://docs.ogc.org/dis/21-056r10/21-056r10.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/GeoPose](https://github.com/ogcincubator/GeoPose)
* Path: `bblocks/_sources/basic/ypr`
