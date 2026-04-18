# Troubleshooting Report – Small Company Network

## Issue 1: Switch Port State Issues
- **Problem:** Fa0/1 initially showed down/down state
- **Cause:** Physical link or initialization issue in Packet Tracer
- **Fix:** Cable reset and `no shutdown` applied

---

## Issue 2: VLAN Communication Failure
- **Problem:** PCs could not communicate across VLANs
- **Cause:** Incomplete trunk or routing verification during setup
- **Fix:** Verified 802.1Q trunk configuration and router subinterfaces

---

## Issue 3: Packet Loss During Inter-VLAN Testing
- **Problem:** Intermittent ping success (3/4 replies)
- **Cause:** ARP instability and network convergence delay
- **Fix:** Cleared ARP tables and retested connectivity

---

## Debugging Methodology Used

- Layer-by-layer testing (L1 → L3)
- Incremental ping testing (gateway first, then cross-VLAN)
- Verification using Cisco CLI show commands
- Endpoint validation (PC IP + gateway checks)

---

## Key Learning

The most critical insight was that network issues are not always configuration errors — they can also be caused by incomplete convergence, endpoint misconfiguration, or physical-layer simulation issues.