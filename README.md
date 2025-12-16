# FluxHarbor

Built for Base

FluxHarbor is a compact Base-oriented repository designed to verify network access, wallet connectivity, and explorer visibility using official Coinbase and Base tooling.

The project favors clarity and inspection over application complexity, making it suitable for repeated Base environment checks and lightweight demos.

---

## Network Scope

The repository operates against two Base networks:

Base Mainnet  
- chainId (decimal): 8453  
- Explorer: https://basescan.org  
- Public RPC: https://mainnet.base.org  

Base Sepolia (testnet)  
- chainId (decimal): 84532  
- Explorer: https://sepolia.basescan.org  
- Public RPC: https://sepolia.base.org  

---

## What FluxHarbor Does

Primary file: `app/fluxHarbor.ts`

At runtime, FluxHarbor:
- Boots an OnchainKit provider bound to a selected Base chain
- Displays wallet onboarding UI through OnchainKit Wallet
- Uses a Viem public client to perform Base RPC reads
- Retrieves:
  - chainId as reported by RPC
  - latest block number
  - native ETH balance for a provided address
- Exposes direct Basescan links for manual verification

---

## Repository Layout

- app/
  - fluxHarbor.ts  
    React entry point combining wallet UX with Base JSON-RPC reads.

Typical supporting files:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

---

## Dependencies

- OnchainKit  
  Wallet UI components and Base-first primitives  
  https://github.com/coinbase/onchainkit  

- Viem  
  EVM client used for Base onchain reads  

---

## Setup Notes

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies with your preferred package manager and run via a standard React/Vite or Next.js development server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

---

## Base Mainnet Deployment

Deployed on Base Mainnet

Network: Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Deployed contract address:  
your_adress  

Basescan deployment and verification links:
- Contract address:  
  https://basescan.org/address/your_adress  
- Contract verification (source code):  
  https://basescan.org/address/your_adress#code  

---

## License

MIT License

---

## Author

GitHub: https://github.com/shadowdames 

Public contact (email): dames.shadow-0l@icloud.com 

Public contact (X): https://x.com/fedorovmaxx1

---

## Testnet Deployment (Base Sepolia)

For staging and validation purposes, multiple contracts can be deployed on Base Sepolia to exercise Base-compatible tooling before mainnet usage.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0x0dc2d16295a378ec37235edb8010554775aa5aff 

Deployment and verification:
- https://sepolia.basescan.org/address/0x0dc2d16295a378ec37235edb8010554775aa5aff 
- https://sepolia.basescan.org/0x0dc2d16295a378ec37235edb8010554775aa5aff0#code  


These testnet deployments help validate Base RPC reliability, account abstraction–related flows, and read-only onchain behavior in a controlled environment prior to Base Mainnet deployment.

