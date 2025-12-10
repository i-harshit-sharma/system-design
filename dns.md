## DNS

### Overview
DNS (Domain Name System) is a hierarchical system that translates human-readable domain names (like `example.com`) into IP addresses (like `192.0.2.1`).

When a browser is making a dns query, it may be asking a domain name server(dns resolver) like ISP or DNS service providers like Google DNS `8.8.8.8` or Cloudflare DNS(`1.1.1.1`).

If the DNS record is not available or is expired at the DNS resolver, It has to query the authoritative DNS server for the domain name.

**Authoritative DNS Server** An authoritative DNS server is a server that holds the DNS records for a domain. When we update DNS records, we update them here.

But how do we find it?

There are 3 main levels of DNS servers:

> 1.  Root DNS Servers - Has the IP of the TLD name servers (13 in the world)
> 2.  TLD Name Servers - Has the IP of the Authoritative DNS servers (for .com, .org, .net, etc.)
> 3.  Authoritative DNS Servers 


### DNS Records
DNS records are used to map domain names to IP addresses and other resources. Some common types of DNS records include:

- **A Record**: Maps a domain name to an IPv4 address.
- **AAAA Record**: Maps a domain name to an IPv6 address.
- **CNAME Record**: Maps a domain name to another domain name (alias).
- **MX Record**: Specifies the mail servers for a domain.
- **TXT Record**: Used to store text information, often for verification purposes.
- **NS Record**: Specifies the authoritative name servers for a domain.
### DNS Resolution Process
1. The user types a domain name into their browser. 
2. The browser checks its cache for the IP address.
3. If not found, the browser asks the operating system's DNS resolver.
4. The DNS resolver checks its cache for the IP address.
5. If not found, the DNS resolver queries a Root DNS server.
6. The Root DNS server responds with the TLD name server for the domain.
7. The DNS resolver queries the TLD name server.
8. The TLD name server responds with the authoritative DNS server for the domain.
9. The DNS resolver queries the authoritative DNS server.
10. The authoritative DNS server responds with the IP address.
11. The DNS resolver caches the IP address and returns it to the browser.
12. The browser caches the IP address and establishes a connection to the web server.

### How to update a DNS Record
First reduce the TTL (Time to Live) of the DNS record you want to change to a low value. This ensures that the change propagates quickly. Then update.
