---
layout: theme-minimal.njk
title: Network Configuration
---

## Radio Parameters

All nodes in the mesh must be configured with identical radio settings. Mismatched parameters will prevent communication.

| Parameter        | Value       |
|------------------|-------------|
| Frequency        | 869.431 MHz |
| Bandwidth        | 62.5 kHz    |
| Spreading Factor | SF6         |
| Coding Rate      | CR5         |

## Regional Settings

Due to its experimental and bleeding-edge nature, this mesh uses the **strict regions** functionality. A repeater or companion not using regions when sending messages will not be forwarded by the mesh.

> All repeaters must have regions configured before joining the mesh.

The full list of available region identifiers can be found on [meshwiki.nl](https://meshwiki.nl/wiki/Lijst_van_regio%27s). The example below is for Amsterdam specifically — replace the region identifiers with those appropriate for your location, but keep the structure (`put`, `allowf`, `denyf`, `save`) intact.

```
region put nl
region put nl-nh
region put nl-ams
region allowf nl
region allowf nl-nh
region allowf nl-ams
region denyf *
region save
```

## Multi-byte Paths

All repeaters and companions are encouraged to enable multi-byte paths. This improves routing efficiency across the mesh. To enable it on a repeater, run the following command:

```
set path.hash.mode 1
```
