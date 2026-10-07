# IndustrialCraft — WAX Frontend

Frontend application for the IndustrialCraft blockchain project running on the WAX network.

The application is built with React and TypeScript and provides the user interface for interacting with the IndustrialCraft smart contract and WAX blockchain.

## Tech Stack

### Frontend

- React 18
- TypeScript
- React Router
- React Bootstrap
- Bootstrap

### State Management

- Redux
- Redux Toolkit
- Redux Thunk

### Blockchain

- WAXJS
- Anchor Link
- Anchor Browser Transport

### Networking

- Axios

### Development Tools

- ESLint
- Prettier
- Husky
- lint-staged
- React Testing Library

## Project Overview

IndustrialCraft is a blockchain-based digital asset application built on the WAX network.

The frontend provides the user-facing interface and communicates with the WAX blockchain by constructing and sending blockchain transactions.

```text
User
  ↓
React / TypeScript UI
  ↓
Redux State
  ↓
Transaction Layer
  ↓
Wallet / WAXJS / Anchor
  ↓
IndustrialCraft Smart Contract
  ↓
WAX Blockchain
```

The blockchain business logic itself is implemented in a separate C++ smart-contract repository.

## Main Features

The frontend includes:

- React-based user interface
- TypeScript type safety
- client-side routing
- global application state with Redux
- WAX blockchain integration
- blockchain transaction handling
- wallet-related blockchain interaction
- reusable application components
- separate landing and application pages
- dedicated transaction/API layer
- integration with the IndustrialCraft smart contract

## Project Structure

```text
WAX_Project_front/
│
├── public/
│
├── src/
│   │
│   ├── api/
│   │   └── transact.api.ts
│   │
│   ├── assets/
│   │
│   ├── components/
│   │   ├── Landing/
│   │   └── Play/
│   │
│   ├── pages/
│   │   ├── LandingPage/
│   │   └── PlayPage/
│   │
│   ├── redux/
│   │   ├── user/
│   │   └── store.ts
│   │
│   ├── types/
│   │   └── index.ts
│   │
│   ├── App.tsx
│   └── index.tsx
│
├── package.json
├── tsconfig.json
├── .eslintrc.json
├── .prettierrc.json
└── README.md
```

## Application Architecture

The application separates UI, state management, and blockchain communication.

```text
┌──────────────────────────────┐
│            User              │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      React Components        │
│                              │
│  Landing / Play interfaces   │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│        Redux Store           │
│                              │
│  Application / user state    │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      Transaction Layer       │
│      transact.api.ts         │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     WAXJS / Anchor Link      │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│    IndustrialCraft Contract  │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│        WAX Blockchain        │
└──────────────────────────────┘
```

## Pages

The application contains two main page areas.

### Landing Page

```text
src/pages/LandingPage/
```

Contains the public-facing entry point of the application.

### Play Page

```text
src/pages/PlayPage/
```

Contains the main application interface used for interacting with the blockchain-based application.

## Components

Reusable UI components are organized into:

```text
src/components/Landing/
src/components/Play/
```

This keeps page-level components separated from reusable interface elements.

## Blockchain Transaction Layer

Blockchain transaction logic is separated from UI code in:

```text
src/api/transact.api.ts
```

This layer is responsible for handling communication between the frontend and WAX blockchain infrastructure.

Separating transaction logic from React components keeps blockchain interaction easier to maintain and reuse.

## State Management

Redux is used for shared application state.

The Redux configuration is located in:

```text
src/redux/store.ts
```

User-related state is separated into:

```text
src/redux/user/
```

The project uses Redux Toolkit and Redux Thunk for state management and asynchronous actions.

## TypeScript

Shared application types are stored in:

```text
src/types/index.ts
```

TypeScript is used throughout the project to improve type safety and make data structures and component interfaces more explicit.

## Getting Started

### Requirements

Install:

- Node.js
- npm

Clone the repository:

```bash
git clone https://github.com/Sunnez/WAX_Project_front.git
```

Move into the project directory:

```bash
cd WAX_Project_front
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm start
```

The React development server will start locally.

## Production Build

Create a production build with:

```bash
npm run build
```

The optimized application will be generated in the build directory.

## Testing

Run the test suite with:

```bash
npm test
```

The project uses React Testing Library and Jest tooling provided by Create React App.

## Code Quality

The repository includes several development tools for maintaining consistent code quality.

### ESLint

Used for static code analysis and detecting common JavaScript / TypeScript issues.

### Prettier

Used for automatic code formatting.

### Husky

Used for Git hooks.

### lint-staged

Runs formatting and linting commands on staged files before commits.

This helps keep formatting and code style consistent across the project.

## Smart Contract Backend

The blockchain backend for the application is implemented as a C++ smart contract.

Repository:

https://github.com/Sunnez/WAX_Project_back

The backend repository contains:

- C++ smart-contract source code
- WAX blockchain logic
- user actions
- contract-level actions
- AtomicAssets integration
- compiled WASM contract
- ABI contract interface

## Full Application Flow

```text
User
 ↓
React UI
 ↓
Redux / Application State
 ↓
Transaction API
 ↓
WAXJS / Anchor
 ↓
User Wallet
 ↓
Signed Blockchain Transaction
 ↓
IndustrialCraft C++ Smart Contract
 ↓
WAX Blockchain
```

## What This Project Demonstrates

This project demonstrates practical experience with:

- React
- TypeScript
- component-based frontend architecture
- Redux state management
- asynchronous frontend workflows
- blockchain integrations
- wallet / transaction workflows
- API and transaction abstraction
- communication between a web application and a smart contract
- development tooling with ESLint, Prettier and Husky
