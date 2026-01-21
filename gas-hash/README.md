# Ethereum Gas Fee and Merkle Root Calculator


## Overview
This repo contains:
- Simple explanations of key concepts around gas.
-  TypeScript scripts for computing the Merkle roots of transactions using SHA256 and Keccak256.

## Gas Fees in Ethereum: Explanation and Formula

In Ethereum (and similar EVM-based blockchains), gas is a unit that measures the computational effort required to execute operations in a transaction or smart contract. 
It prevents spam and ensures fair resource allocation on the network. Gas fees are the costs associated with these operations, paid in ETH (or the native token).

In Ethereum and similar blockchains, gas is a unit for measuring computational effort required to execute operations in a transaction or smart contract. It helps to reduce spam and ensure fair resource allocation on the network. Gas fees are the costs associated with these operations, paid in **ETH** (or the native token).

I'll like to explain some concepts that are closesly associated with gas.

### Key Concepts 
- **Gas Limit**: This is the maximum amount of gas a transaction is allowed to use/consume, usually set by the user when submitting the transaction. If the transaction exceeds the limit in for a transaction, it fails and the gas is used. 
- **Gas Price**: This is the price/unit (Gwei, where 1 Gwei = 10^-9 ETH) of gas that the user bids. Miners will usually prefer a higher gas price.
- **Gas Used**: The actual amount of gas consumed by the transaction after it has been executed.

- **Base Fee**: This fee is dynamically adjusted by the protocol depending on how the network is congested. It would watch for the block to be ~50%. This fee is burned, and ETH suply is reduced.
- **Priority Fee**: An optional extra fee to incentivize miners/validators to include your transaction faster.
- **Effective Gas Price**: The total price per gas unit paid = Base Fee + Priority Fee.

**Total Gas Fee = Gas Used x Effective Gas Price** 

Other variables influencing gas fees include

Network Congestion: High demand raises base fee.

Gas fees are not fixed; they're market-driven.


## Markle Root
This is a cryptographic hash that serves as a unique fingerprint for all transactions within a blockchain block. It is the final code in a markle tree.


### Setup
run
```bash
  git clone https://github.com/Olorunshogo/blockheader-web3-assignments.git
  cd gas-hash
  npm install
  node hash.ts
```

## Merkle Root
- Prompts for tx count and strings, derives hashes, computes roots with both algorithms.
- Leaves are 64-char hex (32 bytes).

## Notes
- Tested on Node.js 24.11.1.