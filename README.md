![Bitcoin Cash Name Service](./assets/title.jpg)

> 📙🔍 Documents and implementations for the Bitcoin Cash Name Service.

## 💡 What is Bitcoin Cash?
Bitcoin Cash is an experimental digital currency that enables instant payments to anyone, anywhere in the world. It uses peer-to-peer technology to operate with no central authority: managing transactions and issuing money are carried out collectively by the network. Bitcoin Cash is a descendant of Bitcoin. It became a separate currency from the version supported by Bitcoin Core when the two split on August 1, 2017. Bitcoin Cash and the Bitcoin Core version of Bitcoin share the same transaction history up until the split.

## 💡 What is BNS?
BNS – or blockchain name system – is the protocol on the internet that turns human-comprehensible decentralized website names such as ‘website.bch or ‘mywebsite.eth’ into addresses understandable by decentralized network machines.

## 📝 Description

BCNS is the Bitcoin Cash Name Service, a distributed, open, and extensible naming system based on the Bitcoin Cash blockchain.
BCNS eliminates the need to copy or type long addresses. With BNS, you'll be able to send token to anyone at 'yourfriend.bch' instead of 'qrd9khmeg4nqag3h5gzu8vjt537pm7le8...', interact with your favorite contract at 'mycontract.bch', or visit an IPFS-hosted site at 'mywebsite.bch’.

## Technical Overview

BNS is a portable Omni Layer implementation that is based on the Bitcoin ABC codebase. This implementation requires no external dependencies extraneous to Bitcoin ABC, and is native to the Bitcoin Cash network just like other Bitcoin Cash nodes. BNS Layer extensions are exposed via the JSON-RPC interface.

## 📁 Documents

#### Table of Contents
-  [Introduction](./docs/INTRODUCTION.md)
-  [BNS Protocol](./docs/BNS_PROTOCOL.md)
-  [Implementation](./docs/IMPLEMENTATION.md)
    - [Registry](./docs/REGISTRY.md)
    - [Registrar](./docs/REGISTRAR.md)
    - [Resolver](./docs/RESOLVER.md)
-  [Integration](./docs/INTEGRATION.md)

## 📚 BCNS Spec

### Transaction Field Definitions

This section defines the fields that are used to construct transaction messages.

#### Field: Ecosystem
- Description: Specifies the ecosystem of BCNS
- Size: 8-bit unsigned integer, 1 byte
- Valid values: 1

#### Field: Integer-one byte
- Description: used as a multiplier or in other calculations
- Size: 8-bit unsigned integer, 1 byte
- Valid values: 0 to 255

#### Field: UTC Datetime
- Description: Datetime, assuming UTC timezone (the same timezone used by the bitcoin blockchain)
- Size: 64-bits standard unix timestamp, 8 bytes (note: seconds, not milliseconds)

#### Field: Property type
- Description: Specifies the type of BCNS.
- Size: 8-bit unsigned integer, 1 byte
- Valid values:
    - 1: Domain name is available
    - 3: Domain name is taken and currently owned by someone
    - 4: Domain name is forbidden

#### Field: Bitcoin Address
- Description: the 21 bytes needed to uniquely identify a bitcoin address
- Size: 21 bytes, binary data
- Valid values: any 21 bytes (version + output of RIPEMD-160 hash step of creating a bitcoin address)

#### Field: Transaction version
- Description: Description: the version of the transaction definition, monotonically increasing independently for each transaction type
- Size: 16-bit unsigned integer, 2 bytes
- Required/optional: Required
- Valid values: 0 to 65535

#### Field: Transaction type
- Description: the MSC Protocol function to be performed
- Size: 16-bit unsigned integer, 2 bytes
- Current Valid values:
    - 0: Register a domain
    - 30: Set domain owner
    - 31: Create BCNS subdomain
    - 32: Set domain resolver
    - 33: Set domain time to leave
    - 50: Set address associate with domain
    - 51: Set content associate with domain
    - 52: Set multihash associate with domain
    - 53: Set name associate with domain
    - 54: Set text associate with domain(key-value pair)

## 📣 Contributing
See [CONTRIBUTING.md](./CONTRIBUTING.md) for how to help out.

## 🗒 Licence
See [LICENSE](./LICENSE) for details.
