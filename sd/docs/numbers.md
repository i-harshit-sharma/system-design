---
sidebar_position: 1
---

# Numbers every System Designer should know

| Time Range     | Operation                                                      |
| -------------- | -------------------------------------------------------------- |
| < 1 ns         | Data transfer among CPU Registers                              |
| 1 - 10 ns      | L1 and L2 Cache access                                         |
| 10 - 100 ns    | L3 Cache access, DRAM access(Lower limit)                      |
| 100 ns - 1 µs  | DRAM access (Upper limit), MD5 Hash, System call               |
| 1 µs - 10 µs   | Copying 64 KB in memory, Context switch                        |
| 10 µs - 100 µs | Network Proxy, 1 MB data read from SSD                         |
| 100 µs - 1 ms  | Intra zone network latency, SSD write delay                    |
| 1 ms - 10 ms   | Inter zone network latency, Rotational disk seek, Memcache get |
| 10 ms - 100 ms | DNS lookup, 1GB data read from Main memory                     |
| 100 ms - 1 s   | Bcrypt hash, TLS handshake                                     |
| > 1 s          | Transfer 1 GB over a network in same region                    |
