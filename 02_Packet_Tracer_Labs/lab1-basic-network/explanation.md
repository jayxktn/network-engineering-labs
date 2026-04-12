# Lab 1: Basic Network Setup

## Objective

To connect two PCs through a switch and verify communication.

## Topology

* 2 PCs
* 1 Switch

## Configuration

PC1:

* IP: 192.168.1.1
* Subnet: 255.255.255.0

PC2:

* IP: 192.168.1.2
* Subnet: 255.255.255.0

##  Results

Ping between PC1 and PC2 was successful.

## Failure Scenario

Changed PC2 subnet mask to 255.255.0.0, which can cause network misinterpretation.

##  Troubleshooting

* Checked IP settings
* Verified subnet mask
* Used ping to test connectivity

##  Key Learning

Devices must be in the same subnet to communicate directly without a router.
