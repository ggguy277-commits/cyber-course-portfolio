# Network Profile — [my machine]

## Identity
- IPv4 address: 10.210.172.xxx
- Subnet mask / CIDR: 255.255.248.0
- MAC address: E8-65-38-21-69-xx
- Network address: 10.210.168.0
- Broadcast address: 10.210.168.255

## Gateway and reachability
- Default gateway: 10.210.168.1
- Ping to gateway (avg): 9 ms
- Ping to 1.1.1.1 (avg): 100% packet loss

## DNS
- Configured DNS server(s): 62.241.198.245  62.241.198.246
- example.com resolves to: 104.20.23.154

## Path to the internet
- Hops to example.com: 172.66.147.243
- First hop: 10.210.168.1 6 ms, 20 ms, 5 ms

## Listening ports
| Port | Protocol | Interface (localhost / all) | Common use |
|------|----------|------------------------------|------------|
| 135  | TCP      | All (0.0.0.0)                | Microsoft RPC Endpoint Mapper (core Windows service)|
| 139  | TCP      | Specific IP (10.210.172.161) | NetBIOS Session Service (legacy Windows file sharing)|
| 445  | TCP      | All (0.0.0.0 / [::])         | SMB / Direct Host (Windows file and printer sharing)|
| 5040 | TCP      | All (0.0.0.0)                | Windows Network Connection Broker / Delivery Optimization|
|42050 | TCP      | Localhost ([::0])            | Dynamic ephemeral port (internal app/service communication)|
|49635 | TCP      | Localhost (127.0.0.1)        | Dynamic ephemeral port (internal local app communication)|
|49664–49670| TCP      | All (0.0.0.0 / [::])         | Windows RPC dynamic port range (used by core system services)|

## Reflection (150–200 words)
- What surprised you about your own network?
- Which open port (if any) would you want to investigate or close?
- Which command do you think you'll use most often, and why?


Reviewing my network scan revealed surprising insights into system behavior. I was surprised by the number of high-numbered dynamic ports (49664–49670) open across all interfaces (0.0.0.0). I assumed only user-launched applications opened ports, but Windows continuously runs background listeners for core services.

The port I would investigate most closely is Port 445 (SMB). While useful for local file and printer sharing, exposing file-sharing protocols to public or untrusted networks creates unnecessary security risks if not properly filtered by a firewall.

The tool I will use most often is netstat -ano | findstr LISTENING. It provides an immediate list of active network entry points paired with Process IDs (PIDs). Pairing this command with tasklist or Task Manager makes identifying mystery services straightforward, making it an indispensable first step for basic network security and troubleshooting.
