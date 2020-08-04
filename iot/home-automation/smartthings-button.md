---
title: SmartThings Button
description: 
published: true
date: 2020-08-04T04:14:10.730Z
tags: iot, ha, smartthings
editor: markdown
---

# SmartThings Button

<a href="https://www.samsung.com/us/smart-home/smartthings/buttons/samsung-smartthings-button-gp-u999sjvleaa/"><img align="right" src="https://support.smartthings.com/hc/article_attachments/360002610903/SmartButton_01_0000400.png" style="zoom:50%;padding-right:48px" alt="SmartThings Button"/></a>

- Protocol: Zigbee
- Functions
  - single press
  - double press
  - long press
  
| event | function
| ----  | -----------
| 1001  | long press
| 1002  | single press
| 1004  | double press


## Example event
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
