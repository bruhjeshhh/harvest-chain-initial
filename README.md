# HarvestChain 🌾

A decentralized, blockchain-based marketplace that lets farmers sell their produce directly to buyers. This ensures secure, transparent, and tamper-proof transactions powered by Ethereum smart contracts.

---

## 🚀 Features

-   **Direct transactions** between farmers and buyers.
-   **Transparent and tamper-proof records** stored on the blockchain.
-   **Local test environment** using Ganache for development.
-   **Smart contracts** built with Solidity.
-   **Web interface** powered by Web3.js.
-   **Deployment and testing** managed with Truffle.

---

## 🛠️ Tech Stack

-   **Blockchain**: Ethereum, Solidity, Ganache
-   **Smart Contract Framework**: Truffle
-   **Frontend**: HTML, JavaScript, Web3.js
-   **Dev Tools**: Node.js, npm

---

## 📁 Project Structure\
HarvestChain/
├── contracts/ # Solidity smart contracts
│   └── Marketplace.sol
├── migrations/ # Deployment scripts for Truffle
├── src/ # Frontend code
│   ├── index.html
│   └── app.js
├── test/ # Smart contract tests
├── truffle-config.js # Truffle configuration file
└── README.md

---

## 🧪 How to Run Locally

### Prerequisites

-   [Node.js](https://nodejs.org/en/) and [npm](https://www.npmjs.com/)
-   [Ganache](https://trufflesuite.com/ganache/) (GUI or CLI)
-   [Truffle](https://trufflesuite.com/truffle/)

### Steps

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/bruhjeshhh/HarvestChain.git](https://github.com/bruhjeshhh/HarvestChain.git)
    cd HarvestChain
    ```
2.  **Install dependencies**
    ```bash
    npm install
    ```
3.  **Start Ganache**
    
    You can either open the Ganache GUI and start a workspace, or run the following command in your terminal:
    ```bash
    ganache-cli
    ```
4.  **Compile and deploy smart contracts**
    ```bash
    npx truffle compile
    npx truffle migrate
    ```
5.  **Open frontend**
    
    Open `src/index.html` in your browser. It will automatically connect to your local Ganache blockchain using Web3.js.

---

## 📜 Smart Contract Overview

### `Marketplace.sol`

-   **Farmers** can list products with a name, price, and quantity.
-   **Buyers** can purchase products by calling smart contract functions.
-   The contract emits **events** for all major actions (listing, purchasing, etc.).
-   All logic and data are stored on-chain, utilizing Ganache as a local blockchain.

#### Example Truffle Console Interaction:

```bash
npx truffle console
> let instance = await Marketplace.deployed()
> await instance.listItem("Wheat", 100, 5)
> await instance.buyItem(0, { value: web3.utils.toWei("0.5", "ether") })
```
🖼️ Demo

This application is not hosted online. To see it in action, you can follow the local setup instructions above. For presentations or demos, it's recommended to include screenshots or a short video.

Created by Brajesh Mohanty and friends

📧 mohantybrajesh4@gmail.com
