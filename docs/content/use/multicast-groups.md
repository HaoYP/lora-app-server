---
title: Multicast-groups
menu:
    main:
        parent: use
        weight: 8
---

# Multicast-groups

By creating a multicast-group, it is possible to send a single downlink payload
to a group of devices (the multicast-group). All these devices share the same
multicast-address, session-keys and frame-counter.

After creating a multicast-group, it is possible to assign devices to the group.
Please note that the device must already created (see [devices]({{<relref "devices.md">}})).
Only devices that share the same [service-profile]({{<relref "service-profiles.md">}})
as the multicast-group can be added.

## Provisioning of the device

The provisioning of the multicast-group on the device happens out-of-band.
This means that after adding a device to a multicast-group, you must also
configure the device with the multicast-address, session-keys etc...

## Sending data

Sending data to the multicast-group happens using the [gRPC]({{<ref "/integrate/grpc.md">}})
or [RESTful JSON]({{<ref "/integrate/rest.md">}}) API.
