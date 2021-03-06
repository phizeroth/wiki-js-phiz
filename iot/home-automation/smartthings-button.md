---
title: Samsung SmartThings Button
description: Small, multi-function Zigbee switch
published: true
date: 2020-08-05T05:43:28.372Z
tags: iot, ha, smartthings, zigbee
editor: markdown
---

![smartbutton_01_0000400.png](/smartbutton_01_0000400.png =250x){.align-abstopright}

## Overview

- **Protocol**
  - [Zigbee](https://en.wikipedia.org/wiki/Zigbee)

- **Power**
  - Battery (CR2450 3V)

- **Features**
  - inputs
    - single press
    - long press
    - double press
  - sensors
	  - battery level
	  - temperature

## Setup

After pairing with deCONZ, the device shows up in HassOS as a "button" by manufacturer Samjin, with two entities:
- sensor.button_battery_level
- sensor.temperature
{.grid-list}

> The button functionality itself does *not* show up in HassOS as a device or entity.{.is-info}

In order to capture the button as a trigger, first go to Developer Tools > Events, subscribe and listen to `deconz_event` and press the button to get the `id`:

```json
{
    "event_type": "deconz_event",
    "data": {
        "id": "button_2",
        "unique_id": "28:6d:97:00:01:0d:b7:a4",
        "event": 1002
    },
    "origin": "LOCAL",
    "time_fired": "2020-08-04T03:11:33.404795+00:00",
    "context": {
        "id": "2d7ea8c3001446adade540df2b7715bb",
        "parent_id": null,
        "user_id": null
    }
}
```

Then set up an automation with an event trigger such as:
```yaml
platform: event
event_type: deconz_event
event_data:
  event: 1002
  id: button_2
```

## Available events

action | event id
-|-
long press   | 1001
single press | 1002
double press | 1004

## References
[Manual (pdf)](https://support.smartthings.com/hc/en-us/article_attachments/360002610923/IOT_US_Button_QSG.pdf)

