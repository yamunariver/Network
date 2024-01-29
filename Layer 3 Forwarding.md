## Forwarding IP packets within a LAN: 

1) When a host sending a packet has identified that the destination host is in the same subnet, it can send the packet directly to the destination host

    -> there is no need to send the packet to a router for routing

4) The packet will be encapsulated in an ethernet frame, and the destination MAC address will be the destination host's MAC address

5) The sending host will check its ARP cache for an entry mactching the destination IP. if there is not entry matching the destination IP. If there is no entry. it will send an ARP request
