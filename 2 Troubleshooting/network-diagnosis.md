How to Diagnose Network Connectivity Issues
Overview

Network failure is often the primary reason a deployment or API call fails. This guide outlines a logical "bottom-up" approach to identifying whether a connection issue is local, server-side, or DNS-related.
Audience

System Administrators and DevOps beginners who need to verify server accessibility and internet routing.
Step 1: Verify Local Interface

Check if your own network adapter is active.
PowerShell

ipconfig

Look for a "Default Gateway" IP. If this is empty, you are not connected to a router.
Step 2: Test Server Reachability (Ping)

Verify if the target server is online.
PowerShell

ping google.com

If "Request Timed Out" occurs, the server is either down or blocking ICMP traffic.
Step 3: Trace the Routing Path

Identify where a connection is dropping between you and the server.
PowerShell

tracert 8.8.8.8

If the trace fails at the first few hops, the issue is with your ISP. If it fails at the end, it is a server-side firewall issue.
Step 4: Test Specific Ports (Telnet/Test-NetConnection)

Sometimes the server is "up," but the specific service (like Port 80 for web) is blocked.
PowerShell

Test-NetConnection -ComputerName [Server_IP] -Port 80