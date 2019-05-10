# DDoS: Distributed Denial of Service
 
## DDoS 
 * "starve" good clients by exhausting server resources
 * server resources include CPU, memory, disk, network
 
## Common approaches to defend 
 * ip-based filtering
 * captcha 
 
## Analysis
 * in many cases the CPU/memory/disk is the bottleneck on the server side, not the network; or, the network limit can be more easily addressed
 * bad clients are assumed to send at maximum speed (B), good clients are assumed to send at normal speed (g), B >> g
 * when the server is limited by its CPU/memory/disk, it starts to drop requests randomly.
 * Assume B+g > c, then c*g/(B+g) good requests are processed. Because B >> g, this number is very small.

## Defense by "offense"
 * the system requires each client, no matter good or bad, to issue requests at their maximum speed. So the good clients are issuing at speed G, and G >> g.
 * Assume B+G > c, then c*G/(B+G) good requests are processed. The number is much larger than earlier.
 * If we know B and G, then the idealized capacity we need to handle all good requests would be g(1 + B/G)
 
## Implementations
 * Approach 1: clients repeatedly send requests until fulfilled.
 * Approach 2: clients pay "tax" by uploading a fragment of empty data.

 

