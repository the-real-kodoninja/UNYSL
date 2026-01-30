# UNYSL: (Unyversal Statically Typed Programming Language)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://example.com/build)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://example.com/releases)
[![Discord](https://img.shields.io/discord/1234567890?color=7289da&label=Discord&logo=discord&logoColor=white)](https://discord.gg/unysl)
[![Twitter](https://img.shields.io/twitter/follow/unysl?style=social)](https://twitter.com/unysl)

**UNYSL** (Unyversal Statically Typed Programming Language) is a modern, high-performance language developed by **AVIYON** for building secure, scalable smart contracts and decentralized applications (dApps) on the **Unyversal Liquidity Exchange (ULE)** blockchain network. Designed with developer productivity in mind, UNYSL combines the familiarity of languages like TypeScript, Rust, and Swift with blockchain-specific optimizations, such as actor-based concurrency and orthogonal persistence. It compiles to WebAssembly (Wasm) for efficient execution on ULE nodes, enabling "canister"-style smart contracts that handle state, logic, and data natively without external databases.

UNYSL is a core component of the **ULE Stack**, a comprehensive ecosystem for building seamless mobile, web, and software applications that integrate with the ULE blockchain. Whether you're creating NFT marketplaces, DeFi protocols, or full-stack dApps, UNYSL abstracts blockchain complexities while providing robust tools for multichain interoperability.

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [The ULE Stack](#the-ule-stack)
- [UNYSL vs. Other Languages](#unysl-vs-other-languages)
- [Why UNYSL?](#why-unysl)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Examples](#examples)
- [Development Workflow](#development-workflow)
- [The ULE Ecosystem](#the-ule-ecosystem)
- [Contributing](#contributing)
- [License](#license)

## Overview

UNYSL empowers developers to build "full-stack" decentralized applications where the blockchain serves as both the backend server and persistent storage. Key innovations include:

- **Actor Model**: Smart contracts are independent "actors" that communicate asynchronously, ensuring scalability and fault isolation.
- **Orthogonal Persistence**: Data persists indefinitely in memory-like structures, eliminating the need for traditional databases like SQL or NoSQL.
- **Static Typing**: Catches errors at compile-time with a modern type system supporting generics, enums, pattern matching, and non-nullable types.
- **Blockchain Integration**: Native support for ULE's $ULE token, gas management, and cross-chain operations via the Unyversal SDK.

UNYSL files use `.uny` extensions for core logic and `.html.uny` for frontend templates that embed UNYSL, d30.djs, or lofi.css components. It integrates seamlessly with the broader ULE Stack for end-to-end development.

## Key Features

- **Asynchronous Messaging**: Use `async/await` for non-blocking interactions between canisters.
- **Built-in Persistence**: Variables and data structures (e.g., maps, arrays) are automatically stored on-chain.
- **EVM Compatibility**: Compiles to Wasm but supports Ethereum-like opcodes for hybrid environments.
- **Modular Imports**: Import modules like Python or React, including canister commands and ULE fuel utilities.
- **Security-First Design**: Immutable state by default, with explicit mutability and safe concurrency primitives.
- **Extensibility**: Embed d30.djs (for JavaScript-like logic) and lofi.css (for programmable styling) directly in UNYSL files.

## The ULE Stack

The ULE Stack is a standalone or integrable toolkit for building applications across platforms (mobile, web, desktop). It includes:

| Component          			| Purpose                                                                 																																						 |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Frontend**       			| `.html.uny` templates and `lofi.css` for programmable, low-fidelity CSS. 																																						 |
| **Frontend/Backend** 		| `UNYSL.uny` for logic; `d30.djs` for resilient, JavaScript-like scripting (inspired by D30 impact fluid: flows smoothly but hardens under pressure). |
| **Database/Nodes**      | **Aviyon Cloud**: Serverless, P2P web3 hosting with local nodes and browser/desktop interfaces. 																										 |
| **Blockchain Server**  	| **UNYTE**: Client/server-side rendering for modern JS frameworks (e.g., React, Vue); acts as a local blockchain node for testing. 									 |
| **Infrastructure** 			| **ULE-Protocol**: Decentralized protocol for seamless background integration; **Aviyon Cloud** for cloud-native dev. 																 |
| **Git Integration** 		| **Aviyon Git**: Version control compatible with GitHub, GitLab, etc. 																																								 |
                                                                         
- **Download**: Get the ULE Stack from [ULE.dev](https://ule.dev) (supports Linux, Windows, Mac, Android).
- **Folder Structure Example**:

```

my-app/
├── app/
│   ├── views/
│   │   ├── home/
│   │   │   └── index.html.uny
│   │   ├── settings/
│   │   └── users/
│   ├── controllers/
│   └── assets/
│       └── stylesheets/
│           ├── application.lofi.css
│           ├── global.lofi.css
│           ├── header.lofi.css
│           └── sidebar.lofi.css
├── blockchain/
│   └── canisters/
│       └── counter.uny
└── package.json  # For UNYTE integration

```

The stack supports building everything from simple websites to complex blockchain apps, with automatic integration of ULE-Protocol for decentralization.

## UNYSL vs. Other Languages

| Feature              | UNYSL (ULE)                  | Solidity (Ethereum)          | Motoko (ICP)                 	|
|----------------------|------------------------------|------------------------------|--------------------------------|
| **Primary Goal**     | General-purpose on-chain apps | Financial/token transactions | General-purpose on-chain apps |
| **Data Storage**     | Built-in (automatic persistence) | Manual (state variables/mappings) | Built-in (automatic)	|
| **Communication**    | Asynchronous (async/await)   | Synchronous                  | Asynchronous (async/await)   	|
| **Syntax**           | Functional/OO hybrid         | JavaScript-like with quirks  | Functional/OO hybrid         	|

## Why UNYSL?

- **Simplify Blockchain Development**: Handle state and persistence natively---no need for external servers or databases.
- **Full-Stack on Blockchain**: Frontend and backend live on-chain via canisters.
- **Cost-Efficient Testing**: Use UNYTE for local nodes with fake accounts and zero real gas fees.
- **Multichain Ready**: Integrate with Unyversal SDK for seamless cross-chain interactions.
- **Resilience**: Like d30.djs, UNYSL is "lofi in nature" but "hardens under pressure" for robust performance.

Compared to traditional apps:

| Part of App 	| Language/Tools              	| Role on ULE                                                                 |
|---------------|-------------------------------|-----------------------------------------------------------------------------|
| **Frontend**	| .djs / .html.uny / .lofi.css 	| Served from asset canisters; direct browser rendering.                      |
| **Backend** 	| UNYSL (.uny) / d30.djs      	| Logic canisters handle computations, storage, and async calls.              |
| **Bridge**  	| UNYTE                       	| JS library for frontend-to-backend communication, like a local API.         |

## Installation

1\. **Download ULE Stack**: Visit [ULE.dev](https://ule.dev) and install for your platform.
2\. **Install via CLI**:

   ```

   npm install -g unysl-cli
   unysl-cli init my-project

   ```

3\. **Local Blockchain Setup**:
   - Run `npx unyte node` for a test node (provides 10 accounts with 100 fake $ULE each).
   - For production, connect to Aviyon Cloud nodes.

## Getting Started

1\. Create a new canister:

   ```

   unysl new counter

   ```

2\. Write your UNYSL code in `counter.uny`.
3\. Deploy locally:

   ```

   unysl deploy --network local

   ```

4\. Interact via frontend: Use UNYTE to call canisters from .html.uny or .djs files.

## Examples

### Simple Counter Canister (Backend in UNYSL)

```unysl

// counter.uny
actor Counter {
  // Persistent state: Automatically stored on-chain
  var count: Nat = 0;
  // Public query function (read-only, no gas cost)
  public query func getCount(): async Nat {
    return count;
  };

  // Public update function (modifies state, incurs gas)
  public func increment(): async Nat {
    count += 1;
    return count;
  };

  // Pattern matching example for advanced logic
  public func resetIfHigh(threshold: Nat): async Bool {
    switch (count > threshold) {
      case (true) { count = 0; true };
      case (false) { false };
    };
  };
}

```

### Frontend Integration (.html.uny with Embedded d30.djs)

```html

<!-- index.html.uny -->

<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles.lofi.css">
</head>
<body>
  <h1>UNYSL Counter</h1>
  <button onclick="incrementCounter()">Increment</button>
  <p>Count: <span id="count">0</span></p>
  <!-- Embedded d30.djs script -->
  <script type="d30/djs">
    import { Counter } from '@unysl/canisters/counter'; // UNYTE bridge
    async function incrementCounter() {
      const newCount = await Counter.increment();
      document.getElementById('count').innerText = newCount;
    }
    // Initial load
    async function loadCount() {
      const current = await Counter.getCount();
      document.getElementById('count').innerText = current;
    }
    loadCount();
  </script>
</body>
</html>

```

### Styling with lofi.css

```css

/* styles.lofi.css */
@lofi-theme {
  --primary-color: #007bff;
}

button {
  background-color: var(--primary-color);
  color: white;
  padding: 10px;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: darken(var(--primary-color), 10%);
}

```

Run locally: `npx unyte node` (blockchain) + `npm run dev` (frontend). Open `localhost:5173` and connect via Osmium wallet to `localhost:8545`.

## Development Workflow
- **Local Testing**: Use UNYTE for fake blockchain nodes.
- **Deployment**: Push to Aviyon Cloud for P2P hosting.
- **Version Control**: Integrate with Aviyon Git for seamless GitHub/GitLab sync.
- **Tools**: Oxygen Studio for visual building; CLI for scripting.

## The ULE Ecosystem

UNYSL is part of the broader **Unyversal Liquidity Exchange (ULE)** ecosystem:

- **ULE Network**: Layer 1 blockchain using Cosmos SDK/Polygon CDK for EVM compatibility. Consensus: PoS with NFT-Liquidity-Provisioning (PoL).
- **$ULE Token**: Native gas, governance, and fuel. Features zero-fee listings and 50% fee burns for deflation.
- **ULE-Protocol**: Core engine for liquidity pools, instant exits, and cross-chain routing (via LayerZero/Chainlink CCIP).
- **Unyversal SDK**: Multichain translator for automatic chain detection, gas swaps, and one-click transactions.
- **UnySON**: Connects hardware/software to Aviyon Cloud, unifying the ecosystem.
- **UnyFi**: Joint distribution program for blended liquidity.

**Infrastructure Requirements for Validators**:

| Component 		| Minimum Specification                  |
| ------------- | -------------------------------------- |
| **CPU**   		| 8-Core (high clock speed)              |
| **RAM**   		| 32GB DDR4                              |
| **Storage**		| 2TB NVMe SSD (high IOPS)               |
| **Network**		| 1Gbps redundant connection             |
| **Stake** 		| 100,000 $ULE (self-bond)               |

**Economic Flywheel**: Usage drives $ULE demand, burns supply, and attracts validators for network growth.

**Next Steps**:

1\. Deploy Devnet with $ULE genesis.
2\. Build Unyversal.ts for metadata reading.
3\. Integrate bridges for ULE/ETH.

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Join our [Discord](https://discord.gg/unysl) for discussions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
