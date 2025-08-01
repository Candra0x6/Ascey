# Ascey Platform

## Overview

**Ascey** is a next-generation blockchain platform designed for issuing and managing Real World Asset (RWA) tokens, with a focus on tokenized shares from the EGX30 index. Built on the Internet Computer Protocol (ICP) using the Rust SDK, Ascey combines traditional finance with blockchain technology to deliver secure, transparent, and scalable asset trading and management.

---

## Features

### ⚡ Real-Time Settlement  
Instant transaction finality eliminates delays associated with traditional financial systems.

### 🌍 Fractional Ownership  
Tokenization allows small investors to participate in high-value asset markets via fractional ownership.

### ✅ Regulatory Compliance  
Fully compliant with regulations set by the Financial Regulatory Authority of Egypt, ensuring a secure and trustworthy investment environment.

---

## Business Value

Ascey transforms asset trading by:
- Accelerating transaction speed
- Expanding market access through tokenization
- Integrating decentralized fund management tools into traditional finance

---

## Architecture Overview

Built on the Internet Computer with Rust SDK, Ascey ensures performance, scalability, and decentralization while handling complex financial transactions securely.

### Backend Canisters

#### `ascey_backend`
- **Path**: `src/ascey_backend/ascey_backend.did`  
- **Type**: Rust  
- **Role**: Core logic hub managing token lifecycle, buy/sell operations, swaps, and integration with ledger/index canisters.

#### `xrc`
- **Path**: `xrc/xrc.did`  
- **Role**: Provides real-time exchange rates via aggregated data for accurate pricing.

#### `icrc1_ledger`
- **Path**: Remote  
- **Role**: BELLA token lifecycle management — issuance, transfers, and balances — using the ICRC1 standard.

#### `icrc1_index`
- **Path**: Remote  
- **Role**: Enables transaction querying and indexing for BELLA tokens.

#### `tommy_icrc1_ledger` & `tommy_icrc1_index`
- **Role**: Equivalent functionality to BELLA, specific to the "Tommy" token.

#### `icp_ledger`
- **Path**: Remote  
- **Role**: Handles ICP token transactions including transfers and logging.

#### `icp_index`
- **Role**: Indexes ICP token transactions for transparency and reporting.

#### `internet_identity`
- **Path**: Remote  
- **Role**: Provides decentralized authentication for secure user identity management.

---

### Frontend

- **Type**: Static assets  
- **Role**: UI served via Internet Computer, fully integrated with backend canisters for a seamless user experience.

---

## Getting Started

### Prerequisites

- [Install DFINITY SDK](https://internetcomputer.org/docs/current/developer-docs/setup/install)
- Node.js & npm
- Rust toolchain (`rustup`, `cargo`, etc.)

---

## Project Setup

Run the provided script to initialize the project:

```bash
./setup_project.sh
