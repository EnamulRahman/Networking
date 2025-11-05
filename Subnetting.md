Subnetting

Definition:
Subnetting divides a large network into smaller, manageable networks — improving performance, organization, and security.

CIDR – Classless Inter-Domain Routing

CIDR notation defines how an IP address is divided into network and host portions.
Format:

IP_Address / Prefix_Length
Example: 192.168.1.0/26


Prefix length (/26) → Number of bits used for the network part.

The remaining bits are used for hosts (devices).

How Subnetting Works

🧩 Step 1: IPv4 = 32 bits
Each IP address (e.g., 192.168.1.0) consists of 32 binary bits (1s and 0s).

🧮 Step 2: /26 → 26 bits for network, 6 bits for hosts

Network bits: Identify which subnet the address belongs to.

Host bits: Identify individual devices in that subnet.

🔢 Step 3: Calculate total addresses
Each host bit can be 0 or 1, so:
2⁶ = 64 total addresses

🏠 Step 4: Reserve special addresses

Network address (all 0s): Identifies the subnet (e.g., 192.168.1.0)

Broadcast address (all 1s): Sends messages to all devices (e.g., 192.168.1.63)

Usable addresses: Everything in between.

✅ Summary

Prefix	Host Bits	Total Addresses	Usable	Example Range
/26	6	64	62	192.168.1.1 – 192.168.1.62

Analogy:

The first house (192.168.1.0) is the signpost → network name.

The last house (192.168.1.63) is the loudspeaker → broadcasts to all.

Subnet Mask

A 32-bit value dividing the IP into network and host portions.
Example:
/26 = 255.255.255.192
(26 bits for the network → 255s, remaining bits → 0s)

Network Address Translation (NAT)
Purpose

NAT translates private IP addresses (used inside local networks) into public IP addresses (used on the internet).

It allows multiple devices on a private network to share one public IP.

How NAT Works

Devices inside a home network use private IPs (e.g., 192.168.1.10).

The router translates these into a public IP when accessing the internet.

Replies from the internet are sent back to the router, which forwards them to the correct internal device.

Types of NAT
Type	Description	Example Use
Static NAT	One private IP mapped to one public IP.	Servers needing a fixed external address.
Dynamic NAT	Private IPs mapped to a pool of public IPs.	Businesses with multiple external-facing devices.
PAT (Port Address Translation)	Multiple private IPs share one public IP using different ports.	Home and office networks (most common).

PAT (NAT Overload) example:

192.168.1.10:5001 → PublicIP:80

192.168.1.11:5002 → PublicIP:80
→ The router tracks ports to send replies correctly.

Benefits of NAT

Conserves public IP addresses

Adds a layer of security (hides internal IPs)

Simplifies network design and management

Layer Overview (OSI Reference)
Layer	Name	Function	Examples
1	Physical	Hardware, transmission	Cables, Hubs, Fibre, Wi-Fi
2	Data Link	Node-to-node data (frames)	MAC, Switch, Bridge
3	Network	Routing & IP addressing	IP, Router
4	Transport	End-to-end communication	TCP, UDP, Ports
5	Session	Connection management	Manages sessions
6	Presentation	Data translation & encryption	SSL/TLS
7	Application	User interface	HTTP, HTTPS, DNS
Basic Network Troubleshooting
Command	Purpose	Example
ping	Tests connectivity to a host	ping google.com
traceroute	Shows the path packets take	traceroute google.com
nslookup	Queries DNS for domain details	nslookup google.com
Cloud Networking Concepts

Subnets: Logical divisions of a virtual network.

Virtual Private Cloud (VPC): Isolated section of the cloud network.

Gateways: Connect cloud networks to the internet or other networks.
