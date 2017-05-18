---
layout: page
title: "Telsa Motors"
description: "Instructions for how to integrate Tesla Model S/X into Home Assistant."
date: 2017-05-18 16:00
sidebar: true
comments: false
sharing: true
footer: true
logo: telsamotors.png
ha_category: Hub
ha_release: 0.45
---


The `teslamotors` platform offers integrates with the [Telsa Motors](http://www.volvocars.com/intl/own/connectivity/volvo-on-call) cloud service and offers presence detection as well as sensors such as odometer and battery level.

To use Tesla Motors in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
teslamotors:
  username: username
  password: password
```

A more advanced example for setting the vehicle name and selecting what resources to display:

```yaml
# Example configuration.yaml entry
teslamotors:
  username: username
  password: password
  name:
    abc123: 'Batmobile'
  resources:
    - doors
    - lock
    - heater
```

Configuration variables:

- **username** (*Required*): The username associated with your Volvo On Call account.
- **password** (*Required*): The password for your given Volvo On Call account.
- **name** (*Optional*): Make it possible to provide a name for the vehicles.
- **resources** (*Optional*): A list of resources to display (defaults to all available).

