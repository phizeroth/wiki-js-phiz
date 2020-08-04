---
title: SmartThings Button
description: 
published: true
date: 2020-08-04T05:01:01.029Z
tags: iot, ha, smartthings
editor: markdown
---

![smartbutton_01_0000400.png](/smartbutton_01_0000400.png =250x){.align-abstopright}

# Details
**Protocol**:
- Zigbee

**Features**
- inputs: 3
- sensors
	- battery level
	- temperature

# Functions
Button only shows up as a battery level and temperature sensor in HASS devices. 

| event | function
| ----  | -----------
| 1001  | long press
| 1002  | single press
| 1004  | double press


# Example event
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

# References
[Manual (pdf)](https://support.smartthings.com/hc/en-us/article_attachments/360002610923/IOT_US_Button_QSG.pdf)

