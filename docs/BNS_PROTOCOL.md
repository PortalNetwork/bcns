# BNS Protocol

BNS is a portable Omni Layer implementation that is based on the Bitcoin ABC codebase. This implementation requires no external dependencies extraneous to Bitcoin ABC, and is native to the Bitcoin Cash network just like other Bitcoin Cash nodes. BNS Layer extensions are exposed via the JSON-RPC interface.
  
BNS protocol is based on the Bitcoin Cash transaction, the special opcode `OP_RETURN` in the Bitcoin Cash script is used to append BNS protocol to the opcode. The BNS transaction is a special Bitcoin Cash transaction that uses the same security and validation model as the Bitcoin Cash transaction.  
  
BNS Protocol uses an account model. Each Bitcoin Cash address is an account, and each account can contain multiple Domain Names.  
  
BNS Protocol is deployed on multiple nodes, and the nodes running the BNS Protocol are able to verify transactions. 
Non-compliant BNS Protocol will not be resolved by the BNS node, each BNS node can confirm the transaction data and calculate the final legal status.  
