# 🚰 Full-Stack ERC-20 Token Faucet DApp

A complete **Full-Stack Web3 Token Faucet decentralized application** built using **Solidity, Hardhat, React (Vite), Ethers.js, Docker, and MetaMask**.  
The application allows users to securely request ERC-20 tokens from a faucet contract deployed on the **Ethereum Sepolia Testnet**.

---

## ✨ Features

- ERC-20 token implemented using OpenZeppelin
- Faucet contract to request a fixed number of tokens
- MetaMask wallet integration
- Live token balance updates
- Transaction status feedback (pending, success, failure)
- Cooldown / error handling
- Dockerized frontend deployment
- Health endpoint for automated verification

---

## 🏗️ Architecture Overview

```

User (Browser)
|
| MetaMask
v
Frontend (React + Vite + Ethers.js)
|
| JSON-RPC (Infura)
v
Ethereum Sepolia Testnet
├── Faucet Contract
└── ERC-20 Token Contract

```

---

## 📜 Smart Contracts

| Contract | Address | Network |
|--------|--------|--------|
| Faucet Contract | `0x7da213aF0F48b233E24B48096a4C6c844aD61484` | Sepolia |
| ERC-20 Token (FCT) | `0xE00C56969F49E2EA077E6ed9e4EbfBa2656160b6` | Sepolia |

### 🔗 Etherscan Verification
- Faucet: https://sepolia.etherscan.io/address/0x7da213aF0F48b233E24B48096a4C6c844aD61484
- Token: https://sepolia.etherscan.io/address/0xE00C56969F49E2EA077E6ed9e4EbfBa2656160b6

---

## 📁 Project Structure

```

token-faucet-dapp/
├── contracts/          # Solidity smart contracts
├── scripts/            # Deployment scripts
├── test/               # Hardhat test cases
├── frontend/           # React (Vite) frontend
├── screenshots/        # Application screenshots
├── docker-compose.yml  # Docker configuration
├── hardhat.config.js   # Hardhat configuration
├── .env.example        # Environment variable template
└── README.md

````

---

## 📸 Screenshots

### Application Loaded
![App Loaded](screenshots/01-app-loaded.png)

### Wallet Connected
![Wallet Connected](screenshots/02-wallet-connected.png)

### MetaMask Transaction Confirmation
![MetaMask Confirmation](screenshots/03-metamask-transaction-confirmation.png)

### Transaction In Progress
![Transaction Pending](screenshots/04-transaction-in-progress.png)

### Successful Token Claim
![Successful Claim](screenshots/05-successful-token-claim.png)

### Error / Cooldown State
![Cooldown Error](screenshots/06-error-cooldown.png)

### Health Endpoint
![Health OK](screenshots/07-health-endpoint-ok.png)

### Docker Running
![Docker Running](screenshots/08-docker-running.png)

---

## 🎥 Video Demonstration

📺 **Demo Video:**  
(Add YouTube / Loom link here)

The video demonstrates:
- Wallet connection
- Initial token balance
- Successful token claim
- Cooldown / error handling
- Balance update after confirmation
- Docker startup and health check

---

## ⚙️ Environment Variables

Create environment files using the template below.

### `.env.example`

```env
SEPOLIA_RPC_URL=https://sepolia.infura.io/v3/YOUR_INFURA_KEY
PRIVATE_KEY=YOUR_METAMASK_PRIVATE_KEY
ETHERSCAN_API_KEY=YOUR_ETHERSCAN_API_KEY

VITE_RPC_URL=https://sepolia.infura.io/v3/YOUR_INFURA_KEY
VITE_FAUCET_ADDRESS=DEPLOYED_FAUCET_ADDRESS
VITE_TOKEN_ADDRESS=DEPLOYED_TOKEN_ADDRESS
````

⚠️ **Never commit actual `.env` files**

---

## 🐳 Run Locally with Docker

### Prerequisites

* Docker
* MetaMask extension
* Sepolia test ETH

### Start the Application

```bash
docker compose up --build
```

### Access

* Application: [http://localhost:3000](http://localhost:3000)
* Health Check: [http://localhost:3000/health](http://localhost:3000/health)

---

## 🧪 Verification Checklist

* Wallet connects via MetaMask
* Token balance loads correctly
* Tokens can be requested successfully
* Transaction confirmation shown
* Error state displayed when applicable
* `/health` endpoint returns `OK`
* Docker starts without errors

---

## 🔐 Security Notes

* Built using OpenZeppelin ERC-20
* Minting restricted to authorized faucet
* No private keys exposed in frontend
* Contracts verified on Etherscan




