## Broadcast Domain

A broadcast domain is a logical division of a network in which all nodes can reach each other bu layer 2 broadcast 

  -> a group of devices which will receive a broadcast frame sent by any one of the other devices 
  
All devices connected to a switch are in the same broadcast domain; switches flood broadcast frames 

  -> Vlans can be used to divide up broadcast domains on a switch

Each router interface is a unique broadcast domain; routers do not forward layer 2 broadcast messages

### Layer 2 forwarding 

Some CCNA students ask why routers need to encapsulate packets within an Ethernet Frame even though routers are supposed to operate `at layer`. 

Routers use Layer 3 information to decide where to forward packets, but that doesn't mean they can ignore layer 2

Layer 2 forwarding refers to the process switches use to forward frames within a lan. 

-> although routers operate `at Layer 3`, they still are layer 2 aware as they must inspect the destination MAC address of frames they receive, and use Layer 2 to address frames to the next hop device. 


There are four main message types to be aware of from a layer 2 forwarding perspective

## `Message Type`        `Action`


`Unicast (known)`     `Forward`

`Unicast (unknow)`    `Flood`       `unknown unicast frames flooded within the VLAN`

`Broadcast`           `Flood`        `same for broadcast frames`

`Multicast`           `Flood (by default)`      `Multicast: by default, flood out of all ports except the port frame was received on ( in the same VLAN)`

MAC address table 

# show mac address-table
 
`VLAN`    `Mac Address`        `Type`      `Ports`
    
`All`      `0100.0ccc.cccc`    `STATIC`     `CPU`        `Multicast address for CDP, VTP, DTP, ext`

For example, this first entry, `0100.0ccc.cccc` is a multicast MAC address used for protocols

Switches can only forward frames between ports in the same VLAN
