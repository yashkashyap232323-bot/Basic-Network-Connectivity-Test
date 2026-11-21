# Lab 11: Basic Network Connectivity Test

Cisco Packet Tracer project for the Network Security Practical Lab (MCA).

**Author:** Deepesh Kashyap | **Admission No.:** 2026M01410079 | **Branch:** MCA | **College:** ABES Engineering College, Ghaziabad

## Topology
1 x Cisco 1941 router (R1), 1 x Cisco 2960-24TT switch, 2 x PC, all in 192.168.1.0/24.

| Device | Interface | IP Address | Subnet Mask | Gateway |
|---|---|---|---|---|
| Router0 (R1) | GigabitEthernet0/0 | 192.168.1.1 | 255.255.255.0 | N/A |
| PC0 | FastEthernet0 | 192.168.1.10 | 255.255.255.0 | 192.168.1.1 |
| PC1 | FastEthernet0 | 192.168.1.11 | 255.255.255.0 | 192.168.1.1 |

## Tests (from PC1)
1. `ping 127.0.0.1` (loopback)
2. `ping 192.168.1.11` (own IP)
3. `ping 192.168.1.1` (default gateway)
4. `ping 192.168.1.10` (PC0)

All returned 4/4 replies. A failure test (PC1 set to 192.168.2.11) gave 100% loss because the gateway was outside the PC's subnet; fixed by restoring 192.168.1.11.

## Files
- `Lab11_Connectivity.pkt` - Packet Tracer topology (open with Cisco Packet Tracer)
- `Lab11_Basic_Network_Connectivity_Test_Report.docx` - full project report
