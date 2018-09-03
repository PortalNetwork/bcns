# Introduction

## What is BCNS?
BCNS eliminates the need to copy or type long addresses. With BNS, you'll be able to send token to anyone at 'yourfriend.bch' instead of 'pqkh9ahfj069qv8l6eys...', interact with your favorite contract at 'mycontract.bch', or visit an IPFS-hosted site at 'mywebsite.bch’.
BCNS is to map human-readable names like `portal.bch` to machine-readable identifiers such as Bitcoin Cash addresses, content hashes, and metadata. BCNS also supports `reverse resolution`, making it possible to associate metadata such as canonical names or interface descriptions with Bitcoin Cash addresses.

BCNS has similar goals to DNS, the Internet’s Domain Name Service, but has significantly different architecture, due to the capabilities and constraints provided by the Bitcoin Cash blockchain. Like DNS, ECNS operates on a system of dot-separated hierarchial names called domains, with the owner of a domain having full control over the allocation of subdomains.

Top-level domains, like `.bch` are owned by smart contracts called registrars, which specify rules governing the allocation of their subdomains. Anyone may, by following the rules imposed by these registrar contracts, obtain ownership of a second-level domain for their own use.

## What is Omni Layer?
The Omni Layer is a communications protocol that uses the Bitcoin block chain to enable features such as smart contracts, user currencies and decentralized peer-to-peer exchanges. A common analogy that is used to describe the relation of the Omni Layer to Bitcoin is that of HTTP to TCP/IP: HTTP, like the Omni Layer, is the application layer to the more fundamental transport and internet layer of TCP/IP, like Bitcoin.

## Why we need BCNS?
Blockchain addresses are not friendly enough to humans, the hash addresses are too long, hard to remember, and not easy to identify which is correct or incorrect.  

The blockchain now becomes more and more popular, the shortcomings of address transfer will become more and more obvious. Just as we are sending emails today, it is difficult to use a 32-bit string as an email account. Therefore, an alias service is very helpful for the ease of use of the blockchain system. For example, IPFS has an alias service called InterPlanetary Name Service (IPNS), and Ethereum has its own domain name service called Ethereum Name Service (ENS). We do think that Bitcoin Cash system should also have its own alias service. Called Bitcoin Cash Name Service (BCNS),

## BCNS use cases
The most important use case of the BCNS is for transfer, especially those address that need to disclose their own transfer address and do not change the address frequently.

For example, such as ICO smart contract, the project party needs to disclose its official smart contract address in advance on the official website, but it may be modified by hackers. The address, however, it is difficult for investors to find out which is correct or incorrect. If the project party announces a short and easy-to-remember address alias such as BCNS, the BCNS will be easily recognise, so that the smart contract address can be prevented from being modified by the hacker.

## The Expandability of BCNS
What kind of resource an alias should point to is flexible and can be implemented just by implementing the corresponding BCNS resolvers. In addition to pointing to an address, it can also point to a contract address, thus enabling interaction through BCNS and smart contracts.

## Resources
- [EIP137](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-137.md) - Ethereum Name Service
- [EIP162](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-162.md) - Initial ENS Registrar Specification
- [EIP1062](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1062.md) - Formalize IPFS hash into ENS(Ethereum Name Service) resolver
