---
title: date.millisecond() function
description: >
  The `date.millisecond()` function returns the millisecond of a specified time.
  Results range from `[0-999999]`.
aliases:
  - /influxdb/v2.0/reference/flux/functions/date/millisecond/
  - /influxdb/v2.0/reference/flux/stdlib/date/millisecond/
  - /influxdb/cloud/reference/flux/stdlib/date/millisecond/
menu:
  flux_0_x_ref:
    name: date.millisecond
    parent: date
weight: 301
introduced: 0.37.0
---

The `date.millisecond()` function returns the millisecond of a specified time.
Results range from `[0-999]`.

```js
import "date"

date.millisecond(t: 2019-07-17T12:05:21.012934584Z)

// Returns 12
```

## Parameters

### t {data-type="time, duration"}
The time to operate on.
Use an absolute time, relative duration, or integer.
Durations are relative to `now()`.

## Examples

##### Return the millisecond of a time value
```js
import "date"

date.millisecond(t: 2020-02-11T12:21:03.293534940Z)

// Returns 293
```

##### Return the millisecond of a relative duration
```js
import "date"

option now = () => 2020-02-11T12:21:03.293534940Z

date.millisecond(t: -150ms)

// Returns 143
```
