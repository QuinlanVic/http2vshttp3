# **HTTP/2 vs HTTP/3**
## SDDA – 22 February 2024 
### By: Quinlan Caiger
HTTP/2 and HTTP/3 are different versions of the HTTP (Hypertext Transfer Protocol) network protocol that determines the rules for transmitting data across the internet between servers and clients.
HTTP/2 was established in 2015 and provided a number of benefits over its predecessor HTTP/1.1. For example multiplexing which allowed multiple requests and responses to be transmitted over one TCP connection. 

HTTP/3 inherets all of HTTP/2's features and provides TLS encryption by default (in HTTP/2 it was provided as an optional feature). This extra security reduces the risks of the CIA triad being compromised such as through eavesdropping and MITM attacks. 

#### Some of HTTP/3's other changes and benefits include:
- Getting rid of TCP and using a new type of UDP called QUIC (Quick UDP Internet Connections)
  - QUIC provides the TLS encryption by default (no need for a separate TLS handshake)
- Reduced head-of-line blocking by dealing with each stream level of packet loss (lost packets don’t block all streams of information)
- Improved supporting connection migration meaning that when clients change IP addresses, they don’t lose connectivity or have additional delay
- Zero RTT connection establishment in specific situations (if already connected to a server you can skip the TCP handshake)
- Improved congestion control through advanced mechanisms

HTTP/3 sounds great in theory but is still in development and has not been widely incorporated as it is difficult to implement with compatibility issues surrounding networks.
