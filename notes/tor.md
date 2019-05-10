# Tor: The Onion Routers

## Unsafe communication
 * content ("what") can be intercepted, this can be solved by encryption.
 * source ("who") is known by any router on the link, this is harder to protect.
 
## Tor
 * goal: mask identity of source  
 * trusted: directory server that has the information of the routers
 * untrusted: a router can be hostile, but as long as one router is "good", the communication is safe

## Background: shared secret
 * see this [picture](shared_secret.png)
 * Tor uses this to establish the key for symmetric encryption. (Why not use public/private key scheme? Because it may leak the user's identity.)

## Protocol
 * the user contacts the directory server and selects a set of routers.
 * the user establishes a communication link ("circuit") hop by hop. each router is only aware of the prior router on the circuit. 
 * when the user sends a message over the circuit, the message should be encrypted in layers. Each hop only knows the key to decrypt its own layer.   
 * Each circuit is multiplexed by multiple tap streams. (why? because establishing a circuit costs time.)

## Possible attacks
 * if we can hack into all the routers on a circuit in the order from the destination to the source, we're able to find the source.
 * the attack can also be done by hijacking the network traffic of all routers. 
