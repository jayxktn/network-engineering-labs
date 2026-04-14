## Lab 3:OSPF DYNAMIC ROUTING

## Objective

To enable communication between different networks using OSPF(open shortest path first)instead os static routing.

## Topography

* 2 Routers (R1,R2)
* 2 Switches (S1,S2)
* 4 PCs

## IP Addressing

LAN 1

* Network:192.168.1.0\24
* Gateway:192.168.1.1

LAN 2 

* Network:192.168.1.0\24
* Gateway:192.168.2.1

Router link

* Network: 10.0.0.0\30

## Configureration Summary

* Removed all static routes from both routers
* Enabled OSPF routing process
* Advertised network using OSPF

R1

* OSPF Process ID:1

* Networks:
 
  * 192.168.1.0 0.0.0.255 area 0
  * 10.0.0.0 0.0.0.3 area 0

R2

* OSPF Process ID:1

* Networks:
 
  * 192.168.2.0 0.0.0.255 area 0
  * 10.0.0.0 0.0.0.3 area 0

## How It Works

OSPF allows routers to automatically exchange routing infomation

R1 and R2 form a neighbor relationship over the 10.0.0.0 network.They then share infomation about their connected networks.

Each router builds a routing  table dynamically,allowing packets to be forwarded without manually configured static routes.

## Result

Successful communication between PCs on different networks using OSPF.

Routes were learned dynamically,as shown by "O" entries in the routing table.

## Failure Scenario

If OSPF is not congigured correctly:

* Routers will not form neighbour relationships
* No routers will be exchanged
* Communication between networks will fail

## Troubleshooting

* Verified OSPF config using "show ip route"
* Confirmed routes marked "O"
* Checked interface status using "show ip interface brief"
* Ensure correct wildcard masks were used
* Verified both routers are in the same OSPF area 

## Key Learning

OSPF eliminates the need for manual route configuration by allowing routers to dynamically learn and update routes.

This makes networks more scalable and adaptable compared to static routing.
 
## Challenges Faced

* Troubleshooting when routes did not appear in the routing table

## what i learned

* Verfication commands are essential to confirm correct configurationS
