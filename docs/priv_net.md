# Overview
Developers could follow below steps to setup a private Ionian network, and build Ionian based applications:

1. Setup Ionian smart contract.
2. Run storage nodes.
3. Interact with storage node.

# Setup Ionian smart contract

Ionian smart contract could be deployed on any EVM compatible blockchain, e.g. Ethereum, BSC, polygon and Conflux eSpace. There are several tools (e.g. truffle, hardhat) available to compile the [Ionian smart contract](https://github.com/Ionian-Web3-Storage/ionian-contracts-poc), and deploy bytecodes on blockchain.

On the other hand, [Ionian Client](https://github.com/Ionian-Web3-Storage/ionian-client) also provide [CLI](https://github.com/Ionian-Web3-Storage/ionian-client#cli) to deploy Ionian smart contract on any EVM compatible blockchain.

# Run storage nodes

Developers could clone and compile the Ionian [source code](https://github.com/Ionian-Web3-Storage/ionian-rust) of storage node to generate the executable file. Then, run a storage node with following command:

```
./ionian_node --config node.toml
```

Developers could get started with the [default configuration](https://github.com/Ionian-Web3-Storage/ionian-rust/blob/main/run/config.toml), and configure the necessary parameters for Ionian smart contract:

```
blockchain_rpc_endpoint = "https://xxx-rpc.com"
log_contract_address = "0x1324..."
```

Note, to setup a private Ionian network with multiple storage nodes at local machine, different configurations should be prepared for different storage nodes.

# Interact with storage node

Storage node provides some JSON-RPCs for application/client to interact with. Developers could use the golang [SDK](https://github.com/Ionian-Web3-Storage/ionian-client/blob/main/node/client.go) to build Ionian based applications:

1. Query file info.
2. Upload file segments.
3. Download file segments.

Ionian client also provides some [CLI tools](https://github.com/Ionian-Web3-Storage/ionian-client#cli) to upload or download a file to/from Ionian network. Developers could take these utilities as examples to build their Ionian based applications.
