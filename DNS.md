Domain Name System (DNS)
Purpose

DNS translates human-friendly domain names (e.g., www.google.com) into IP addresses (e.g., 142.250.190.78) that computers use to communicate.

Core DNS Components

1. Name Servers

Store and serve DNS records.

Two main types:

Authoritative Name Server – Holds the actual DNS records for a domain.

Recursive Name Server (Resolver) – Looks up DNS records on behalf of clients.

Example Commands:

dig ns google.com
dig +short ns google.com


→ Returns Google’s authoritative name servers.

2. Zone Files

Text files stored on authoritative servers.

Contain DNS records for a domain in a structured, human-readable format.

Define how the domain should resolve and its related services.

DNS Records (Types)

Each entry in a zone file is a record, containing:

Name: The domain/subdomain (e.g., www)

TTL: Time to live (how long a record is cached)

Class: Usually IN (Internet)

Type: Record type (A, CNAME, MX, etc.)

Data: The value (IP, alias, text, etc.)

Common Record Types:

A Record: Maps a domain name to an IPv4 address.

AAAA Record: Maps a domain name to an IPv6 address.

CNAME (Canonical Name): Points one domain to another.

Example: www.google.com → google.com

MX (Mail Exchange): Directs email to mail servers (includes priority values).

TXT Record: Stores text information, often used for verification or security (SPF, DKIM).

DNS Resolution Process

Analogy: Think of DNS as a chain of “helpers” — each one knows who to ask next.

🧠 Step 1: Client Checks Locally

The client (your computer) checks:

Local DNS cache (recently visited sites).

Hosts file (/etc/hosts on Linux/Mac, C:\Windows\System32\drivers\etc\hosts on Windows).

If found, it stops here.

If not, it queries a DNS Resolver (e.g., your ISP’s or Google’s 8.8.8.8).

📡 Step 2: DNS Resolver Query

The resolver checks its own cache.

If it doesn’t have the record, it begins the lookup process by contacting external servers.

🌍 Step 3: Root Server

Resolver asks a Root DNS Server:
“Where can I find .com domains?”

The Root Server replies:
“Ask the .com TLD Name Servers.”

🏢 Step 4: TLD (Top-Level Domain) Server

The resolver asks the .com registry (like Verisign):
“Where can I find google.com?”

The TLD server responds:
“Ask Google’s authoritative name servers.”

🏠 Step 5: Authoritative Name Server

Resolver asks Google’s name server:
“What is the IP for google.com?”

Response: 142.250.190.78

💾 Step 6: Cache & Return

The resolver stores the answer (based on TTL).

Sends the IP address back to your computer.

The browser connects directly to the destination.

DNS Hierarchy (Summary)
Level	Description	Example
Root Server	Top of the hierarchy	.
TLD Server	Manages top-level domains	.com, .org, .net
Authoritative Server	Holds actual domain data	ns1.google.com
Domain	The specific address	google.com
Tools for DNS Lookups

1. nslookup

Basic DNS query tool for testing domain name resolution.

2. dig (Domain Information Groper)

Advanced tool showing detailed DNS information.

Common commands:

dig google.com
dig +short ns google.com


Non-authoritative answer: Data returned from a cache rather than an authoritative source.

Local Host Files

File: /etc/hosts (Linux/Mac) or C:\Windows\System32\drivers\etc\hosts (Windows)

Maps domain names to IP addresses manually.

Overrides DNS queries.

Useful for testing or local development.

Requires admin permissions to edit.
