# Bitcoin (Proof-of-work)

## A chain of blocks as a public ledger 
 * each block has a header and a body
 * the body has entries of transfers
 * asymmetric encryption scheme (public/private keys) to prevent forging 
 * (hash of) public key as address, private key to sign

## Proof-of-work for consensus
 * each block header contains the hash value of previous block
 * each block's hash must satisfy: the beginning n bits are zero. This is called "difficulty" of the current block. 
 * each block also has a random number, a participant (miner) can enumerate this random number to meet the difficulty requirement. 
 * if the difficulty is n, on average generating each block will take 2^n tries. If the network has "hashing power" as H, and the expected time to generate next block is t. Then: t*H = 2^n. 
 * if the desired time to generate the next block is T, then the difficulty should be set as n=log_2(T*H)


## Forking
 * If two miners both generate (different) next blocks, then the chain "forks". Other clients may accept either chain.
 * Eventually, the longer chain wins, that is, a client will replace its own chain with a new chain if the new chain is longer.
 * 51% attack: if one controls most of the hash powers, she can always rewrite a chain, causing issues such as double spending. 
 * To avoid frequent forking, the expected time to generate a block should not be too small. 4 minutes in bitcoin. To achieve this, the difficulty is adjusted every 2016 blocks (~2 weeks). 
