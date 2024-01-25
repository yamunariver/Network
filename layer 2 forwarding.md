## Broadcast Domain

A broadcast domain is a logical division of a network in which all nodes can reach each other bu layer 2 broadcast   
  -> a group of devices which will receive a broadcast frame sent by any one of the other devices 
  
All devices connected to a switch are in the same broadcast domain; switches flood broadcast frames 
  -> Vlans can be used to divide up broadcast domains on a switch

Each router interface is a unique broadcast domain; routers do not forward layer 2 broadcast messages

### Layer 2 forwarding 



Layer 2 forwarding refers to the process switches use to forward frames within a lan. 

-> although routers operate `at Layer 3`, they still are layer 2 aware as they must inspect the destination MAC address of frames they receive, and use Layer 2 to address frames to the next hop device. 


There are four main message types to be aware of from a layer 2 forwarding perspective

## `Message Type`        `Action`


`Unicast (known)`     `Forward`

`Unicast (unknow)`    `Flood`

`Broadcast`           `Flood`

`Multicast`           `Flood (by default)`
