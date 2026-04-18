# Troubleshooting Report

## Issue 1: Switch Port Down (Fa0/1)
- Problem: Interface was down/down
- Cause: Physical link or shutdown state
- Fix: Reconnected cable and ensured no shutdown

---

## Issue 2: Intermittent Ping Failures
- Problem: Packet loss during inter-VLAN testing
- Cause: ARP instability and incomplete convergence
- Fix: Cleared ARP tables and retested connectivity

---

## Issue 3: Trunk Misconfiguration
- Problem: No inter-VLAN routing initially
- Cause: Incorrect or incomplete trunk setup
- Fix: Configured 802.1Q trunk between switch and router

---

## Commands Used for Debugging
- show ip interface brief
- show vlan brief
- show interfaces trunk
- ping
- arp -d