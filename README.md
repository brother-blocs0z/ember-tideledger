# Ember Tideledger (Built for Base)

Ember Tideledger is a browser-first Base utility focused on validating Base network identity and inspecting public onchain state through strictly read-only operations. It is designed for quick verification, diagnostics, and ecosystem-aligned testing.

---

## Capabilities overview

- Coinbase Wallet connection via EIP-1193  
- Validation of Base-compatible chainIds (8453 / 84532)  
- ETH balance inspection for arbitrary addresses  
- Latest block metadata retrieval  
- Direct Basescan links for independent verification  

No transactions are signed or broadcast.

---

## Repository layout

- app.ember-tideledger.ts  
  Browser entry script handling wallet connection, chain validation, and RPC reads.

- config/networks.json  
  Static configuration describing supported Base networks, RPC endpoints, and explorer URLs.

- docs/architecture.md  
  High-level explanation of project structure, Base alignment, and design decisions.

- docs/validation-notes.md  
  Step-by-step notes used during Base Sepolia testnet validation.

- scripts/sample-addresses.json  
  Example addresses used for repeatable read-only balance and block checks.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - mapping.sol — used for balances, permissions, and ownership
  - ERC20.sol — supports approvals and delegated transfers

- package.json  
  Dependency manifest referencing Coinbase SDKs and multiple Base and Coinbase repositories.

- README.md  
  Technical documentation and deployment records.

---

## Base network context

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

---

## Author

GitHub: https://github.com/rother-blocs0z

Email: brother.blocs0z@icloud.com  

Public contact: https://x.com/MakitiBanana

---

## Tooling and dependencies

This repository integrates tooling from the Base and Coinbase open-source ecosystems:

- Coinbase Wallet SDK for wallet access  
- OnchainKit references for Base-aligned primitives and account abstraction context  
- viem for typed, efficient, read-only RPC communication  
- Multiple Base and Coinbase GitHub repositories included as direct dependencies  

---
## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract mapping.sol address:  
0x211fD755fF016AB6515bA957a1B0bA8285D797AB

Deployment and verification:
- https://sepolia.basescan.org/address/0x211fD755fF016AB6515bA957a1B0bA8285D797AB
- https://sepolia.basescan.org/0x211fD755fF016AB6515bA957a1B0bA8285D797AB/0#code  

Contract ERC20.sol address:  
0xeBf9ee1a9A3a849F951111cde7936FBae424b745

Deployment and verification:
- https://sepolia.basescan.org/address/0xeBf9ee1a9A3a849F951111cde7936FBae424b745
- https://sepolia.basescan.org/0xeBf9ee1a9A3a849F951111cde7936FBae424b745/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.

## License

MIT License

Copyright (c) 2025 YOUR_NAME

---
