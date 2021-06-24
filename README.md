
## SBOM Artifact Image Specification v0.0.0

- [SBOM Artifact Image Specification v0.0.0](#sbom-artifact-image-specification-v000)
  - [Introduction:](#introduction)
  - [Description:](#description)
    - [Overview:](#overview)
    - [Layers:](#layers)
  - [Format:](#format)


### Introduction:

The SBOM (Source Code Bill Of Materials) Artifact Image Specification defines how to bundle SBOMs as OCI images.
SBOM Artifact Images consist of one or more SBOM files, with annotations to indicate which other OCI artifacts, or parts of OCI artifacts, they are intended to cover.

The spec is intended to be generic, allowing for any type of SBOM file, whether it is intended to refer to an OCI image or another type of artifact.

The spec can be considered an extension of the OCI Artifact Spec designed specifically for use by applications which produce and consume SBOM files (as opposed to application containers).
It is intended to be useful to developers and tooling that works with SBOMs and OCI registries.

This document considers primarily the use case of storing WASM Envoy Filters as OCI Images.


### Description:

#### Overview:

The SBOM OCI Artifact Specification defines a method of storing SBOM files which makes them easy to store and distribute, alongside the OCI artifacts they refer to.


#### Layers:

<insert stuff about layers here>

### Format:

Each layer is associated with its own Media Type, which is stored in the OCI Descriptor for that layer:

| Media Type | Type | Description |
|------------|------|-------------|
| text/spdx | SPDX document | An SPDX document. TODO: encoding.
TODO: Cyclone, SWID

`application/vnd.sbom.config.v1+json` Property Descriptions:

| Property   | Type | Description |
|------------|------|-------------|


