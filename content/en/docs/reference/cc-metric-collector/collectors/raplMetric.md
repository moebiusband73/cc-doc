---
title: rapl collector
description: >
  Toplevel raplMetric
categories: [cc-metric-collector]
tags: [cc-metric-collector, Collector, rapl]
weight: 2
---

## `rapl` collector

This collector reads running average power limit (RAPL) monitoring attributes to compute average power consumption metrics. See <https://www.kernel.org/doc/html/latest/power/powercap/powercap.html#monitoring-attributes>.

The Likwid metric collector provides similar functionality.

```json
  "rapl": {
    "exclude_device_by_id": ["0:1", "0:2"],
    "exclude_device_by_name": ["psys"]
  }
```

Metrics:
* `rapl_average_power`: average power consumption in Watt. The average is computed over the entire runtime from the last measurement to the current measurement
