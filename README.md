# Quick-BGP-Troubleshooting-Guide.

![Border Gateway Protocol](https://github.com/user-attachments/assets/383b4994-484f-4d96-b377-3762b5016d39)

A concise step-by-step approach to resolve BGP connectivity issues in under 30 minutes.

Basic BGP Troubleshooting Guide:

If you're facing issues with BGP or connectivity, here's a streamlined troubleshooting approach to resolve it quickly.

Check BGP Neighbor Status:

Use the command show ip bgp summary or show bgp neighbors to check the status of BGP peers. If the status is "Idle" or "Active," there’s a problem with the BGP session.

Verify Network Connectivity:

Ping or traceroute to the BGP peer's IP address. If there’s no response, check the underlying network for issues like routing or link failure.

Verify IP Configuration:

Ensure correct IP address and subnet mask configuration. For IPv4, check that the addresses are in the same subnet if the BGP session is directly connected.

Check BGP Configuration:

Verify that the Autonomous System (AS) numbers and neighbor IPs are correct on both sides. Use show run | include bgp or show ip bgp neighbors to confirm.
Check BGP Authentication (if enabled).

If MD5 authentication is used, ensure that the same password is set on both peers. A mismatch will prevent session establishment.

Ensure TCP Port 179 is Open:

BGP uses TCP port 179. Ensure there are no firewalls or ACLs blocking this port.

Clear BGP Sessions:

If the session is stuck, try clearing it using clear ip bgp <neighbor IP> or clear bgp all.

Check Route Advertisements:

If the session is up but no routes are exchanged, verify that the correct networks are being advertised using show ip bgp.

Restart Devices if Needed:

If all else fails, restarting the router or network equipment can help reset configurations and clear any lingering issues.

This guide should help you resolve BGP-related connectivity issues within 30 minutes.
