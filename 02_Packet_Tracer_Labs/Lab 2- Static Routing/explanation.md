## Lab 2 :Static Routing

## Objective

To enable communication between two diffrent networks using routers and static routing.

## Topology

* 2 Routers (R1,R2)
* 2 Switches (S1,S2)
* 4 PCs

## IP Addressing

Lan 1:

* Network:192.168.1.0/24
* Gateway:192.168.1.1

lan 2:

* Network:192.168.2.0/24
* Gateway:192.168.2.1

RouterLink:

* Network:10.0.0.0/30

## Configuration Summary

*  Assigned IP addresses to all router interfaces
* Enabled interfaces using "no shutdown"
* Configured static routers on both routers

R1:

* Route to 192.168.2.0 via 10.0.0.2

R2:

* Routento 192.168.1.0 via 10.0.0.1

## How It Works

PC1 checks if the destination is in its local network.Since it is not ,it sends the packet to its default gateway(R1).

R1 checks its routing table and finds a static route to the destination network via R2.

R2 receives the packet and forwards it to the correct pc on its local network.

## Result

Successful communication between PCs on diffrent networks using static routing.

## Failure Scenario

When the static route was removed,R1 could not find a path to the destination network and dropped the packet.

## Troubleshooting

* Fixed interfaces that were adminstratively down using "no shutdown"
* Configured clock rate on serial interface
* verified routing using "show ip route"
* verified interfaces using "show ip interface brief"

## Key Learning

Routers require routing informantion to forward packets between networks.without routes, communication fails even if physical connections are workiking

## Challanges Faced

* interface being adminstratively down
* serial connection not working due to missing clock rate
* using commands in the wrong CLI mode (config vs privileged)

## What I Learned From Mistakes

* Always check interface status before troubleshoting routing
* Routing only works if physical and data link layers are functioning
* CLI mode matters when runnning commands like "show"
