# Network Design Overview

## Architecture Choice
A router-on-a-stick design was used to enable inter-VLAN routing using a single physical interface with multiple subinterfaces.

---

## Why VLANs Were Used
- To logically separate departments
- To improve security and reduce broadcast traffic
- To simulate real enterprise segmentation

---

## Why Trunking Was Required
- To carry multiple VLANs over a single link between switch and router using 802.1Q tagging

---

## Scalability Consideration
This design can be extended by:
- Adding more VLANs
- Replacing router with Layer 3 switch
- Implementing DHCP and ACL policies