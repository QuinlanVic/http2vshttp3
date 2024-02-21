# **HTTP/2 vs HTTP/3**
## SDDA – 22 February 2024 
### By: Quinlan Caiger
HTTP/2 and HTTP/3 are different versions of the [HTTP](https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/#:~:text=The%20Hypertext%20Transfer%20Protocol%20(HTTP,of%20the%20network%20protocol%20stack.)) (Hypertext Transfer Protocol) network protocol that determines the rules for transmitting data across the internet between servers and clients.
HTTP/2 was established in 2015 and provided a number of benefits over its predecessor HTTP/1.1. For example, multiplexing which allowed multiple requests and responses to be transmitted over one [TCP](https://www.techtarget.com/searchnetworking/definition/TCP) (Transmission Control Protocol) connection. 

HTTP/3 inherets all of HTTP/2's features and provides [TLS](https://www.cloudflare.com/learning/ssl/transport-layer-security-tls/#:~:text=Transport%20Layer%20Security%2C%20or%20TLS,web%20browsers%20loading%20a%20website) (Transport Layer Security) encryption by default (in HTTP/2 it was provided as an optional feature). This extra security reduces the risk of your informaiton and the [CIA triad](https://www.techtarget.com/whatis/definition/Confidentiality-integrity-and-availability-CIA) being compromised through threats such as eavesdropping and [MITM](https://www.imperva.com/learn/application-security/man-in-the-middle-attack-mitm/) (Man in the Middle) attacks. 

#### Some of HTTP/3's other changes and benefits include:
- Terminating the use of TCP as its transport protocol and adopting a new protocol called [QUIC](https://www.auvik.com/franklyit/blog/what-is-quic-protocol/) (Quick UDP Internet Connections)
  - QUIC is based on the transport protocol [UDP](https://www.cloudflare.com/learning/ddos/glossary/user-datagram-protocol-udp/) (User Datagram Protocol), was initially developed by Google and provides TLS encryption by default
- Reduced head-of-line blocking by dealing with each stream level of packet loss (lost packets don’t block all streams of information)
- Improved supporting connection migration meaning that when clients change IP addresses, they don’t lose connectivity or have additional delay
- Zero [RTT](https://www.cloudflare.com/learning/cdn/glossary/round-trip-time-rtt/#:~:text=round%2Dtrip%20time%3F-,Round%2Dtrip%20time%20(RTT)%20is%20the%20duration%20in%20milliseconds,again%20to%20the%20starting%20point.) (Round-time trip) connection establishment in specific situations (if already connected to a server you can skip the TCP handshake)
- Improved congestion control through advanced mechanisms

#### What does HTTP/3 mean for me?
- Faster connection establishments
- More reliable connections 
- Improved information security

HTTP/3 sounds great in theory but is still in development and has not been widely incorporated as it is difficult to implement with compatibility issues surrounding usage with previous HTTP versions, browser support and existing infrastructure.

##### References:
1. https://gcore.com/learning/what-is-http-3/#:~:text=HTTP%2F3%20establishes%20efficient%20connections,between%20the%20client%20and%20server.
2. https://kiwee.eu/blog/http-3-how-it-performs-compared-to-http-2/
3. https://www.linkedin.com/advice/0/what-benefits-drawbacks-using-http3-over-http2-skills-informatics
4. https://www.cloudflare.com/learning/performance/what-is-http3/
5. https://dev.to/accreditly/http1-vs-http2-vs-http3-2k1c
