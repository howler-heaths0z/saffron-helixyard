# Saffron Helixyard (Built for Base)

Deployed on Base Mainnet.

Saffron Helixyard is a browser-first Base utility that validates Base network identity (chainId 8453 / 84532) and provides a strictly read-only surface for inspecting ETH balances, recent blocks, RPC health, and ERC-20 token metadata with direct Basescan references.

---

## Repository layout

- app/saffron-helixyard.ts  
  Browser script that renders a minimal UI for wallet connection and read-only Base RPC queries.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - storage.sol — minimal contract used to validate deployment and verification flow  
  - mapping.sol — simple stateful contract for interaction testing  
  - imports.sol — lightweight registry contract used for read-only queries  

- package.json  
  Dependency manifest referencing Coinbase SDKs and multiple Base + Coinbase repositories.

- README.md  
  Technical documentation and testnet deployment records.

---

## Base network context

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

---

## Tooling and dependencies

This repository intentionally references both Base and Coinbase open-source ecosystems:

- Coinbase Wallet SDK for EIP-1193 wallet access  
- OnchainKit references for Base-aligned primitives and account abstraction context  
- viem for typed, efficient read-only RPC communication  
- Multiple Base and Coinbase GitHub repositories included via direct Git dependencies  

---

## Capabilities overview

- Connect a Coinbase Wallet and confirm chainId  
- Read ETH balances for any address (read-only)  
- Fetch latest block metadata (timestamp + gas fields)  
- Run an RPC health check (chainId, block height, gas price)  
- Read ERC-20 token metadata and holder balances via standard view methods  
- Output Basescan links for external verification  

No transactions are created, signed, or broadcast.

---

## Usage summary

After installing dependencies and serving the project in a browser:
- Connect a wallet  
- Confirm Base Mainnet or Base Sepolia is active  
- Inspect balances, blocks, and ERC-20 reads  
- Use Basescan links for independent verification  

The application remains fully read-only throughout.

---

## License

MIT License

Copyright (c) 2025 howler-heaths0z

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## Author

GitHub: https://github.com/howler-heaths0z  
Email: howler.heaths0z@icloud.com  
Public contact: https://x.com/lady34545757  

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0xeEa8F8A6c47762DA43c6273ecA522FE60ee71B29

Deployment and verification:
- https://sepolia.basescan.org/address/0xeEa8F8A6c47762DA43c6273ecA522FE60ee71B29
- https://sepolia.basescan.org/0xeEa8F8A6c47762DA43c6273ecA522FE60ee71B29/0#code  

Contract #2 address:  
0x91B0A5c0017b0f7415650E5dC8d703A1cFFB6a50

Deployment and verification:
- https://sepolia.basescan.org/address/0x91B0A5c0017b0f7415650E5dC8d703A1cFFB6a50
- https://sepolia.basescan.org/0x91B0A5c0017b0f7415650E5dC8d703A1cFFB6a50/0#code  

Contract #3 address:  
0xDC67BC3EEBB537D27CB9243295F32B7c30C8Fe66

Deployment and verification:
- https://sepolia.basescan.org/address/0xDC67BC3EEBB537D27CB9243295F32B7c30C8Fe66
- https://sepolia.basescan.org/0xDC67BC3EEBB537D27CB9243295F32B7c30C8Fe66/0#code 
These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
