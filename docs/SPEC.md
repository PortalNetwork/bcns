# BCNS Spec

## Transaction Field Definitions

This section defines the fields that are used to construct transaction messages.

### Field: Ecosystem
- Description: Specifies the ecosystem of BCNS
- Size: 8-bit unsigned integer, 1 byte
- Valid values: 1

### Field: Integer-one byte
- Description: used as a multiplier or in other calculations
- Size: 8-bit unsigned integer, 1 byte
- Valid values: 0 to 255

### Field: UTC Datetime
- Description: Datetime, assuming UTC timezone (the same timezone used by the bitcoin blockchain)
- Size: 64-bits standard unix timestamp, 8 bytes (note: seconds, not milliseconds)

### Field: Property type
- Description: Specifies the type of BCNS.
- Size: 8-bit unsigned integer, 1 byte
- Valid values:
    - 1: Domain name is available
    - 3: Domain name is taken and currently owned by someone
    - 4: Domain name is forbidden

### Field: Bitcoin Address
- Description: the 21 bytes needed to uniquely identify a bitcoin address
- Size: 21 bytes, binary data
- Valid values: any 21 bytes (version + output of RIPEMD-160 hash step of creating a bitcoin address)

### Field: Transaction version
- Description: Description: the version of the transaction definition, monotonically increasing independently for each transaction type
- Size: 16-bit unsigned integer, 2 bytes
- Required/optional: Required
- Valid values: 0 to 65535

### Field: Transaction type
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




