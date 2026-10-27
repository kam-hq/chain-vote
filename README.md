# ChainVote — Decentralized Voting Application

A decentralized voting application built on Ethereum smart contracts with a React frontend. Enables tamper-resistant, transparent voting with real-time result tracking.

## Features

- **On-Chain Voting** — All votes recorded on Ethereum for full transparency
- **Multiple Options** — Create polls with custom options and descriptions
- **Timed Polls** — Set start and end dates for each vote
- **Live Results** — Real-time vote counting with interactive charts
- **MetaMask Integration** — Secure wallet-based authentication
- **Mock Mode** — Test the UI without requiring MetaMask or a blockchain connection

## Tech Stack

| Layer | Technologies |
|---|---|
| **Frontend** | React, TypeScript, Vite, Tailwind CSS, Recharts |
| **Blockchain** | Solidity (0.8.19+), Ethereum, MetaMask |
| **Tooling** | ethers.js, Remix IDE |

## Getting Started

### Prerequisites

- Node.js 18+
- MetaMask browser extension
- Access to an Ethereum network (Sepolia testnet recommended)

### Smart Contract Deployment

1. Open [Remix IDE](https://remix.ethereum.org)
2. Create `VotingContract.sol` and paste the contract code from `contracts/VotingContract.sol`
3. Compile with Solidity 0.8.19+
4. Deploy to your chosen network
5. Copy the deployed contract address

### Frontend Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/kam-hq/chain-vote.git
   cd chain-vote
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Update `CONTRACT_ADDRESS` in `src/lib/contractUtils.ts`

4. Start the development server:
   ```bash
   npm run dev
   ```

## Usage

1. **Connect Wallet** — Click "Connect Wallet" and approve via MetaMask
2. **Create Vote** — Set title, description, options, and start/end dates
3. **Cast Vote** — Select an option and confirm the transaction
4. **View Results** — See real-time charts and voting statistics

## Testing Without MetaMask

The app includes a mock mode with simulated blockchain operations — perfect for UI testing without actual transactions.

## Smart Contract

The contract (`contracts/VotingContract.sol`) supports:
- Creating votes with multiple options
- Secure vote casting (one vote per address)
- Start and end time enforcement
- On-chain participation and result tracking

## Project Structure

```
src/
├── components/     # React UI components
├── lib/            # Contract utilities and helpers
├── hooks/          # Custom React hooks
└── pages/          # Page components
contracts/
└── VotingContract.sol  # Solidity smart contract
```

## License

MIT
