# Quadratic Voting

A semi-decentralized voting system for educational institutions

Schools, Universities, etc.

With one list for the voters and another list for the candidates.

![Preview](hibiscus_quadratic_voting.gif)

## Deployed on Taiko Testnet
https://explorer.jolnir.taiko.xyz/address/0x8CaB06fE2A485A31Cc49795C5C7aC500c698f3e4

## Deployed on Mantle Testnet

https://explorer.testnet.mantle.xyz/address/0x8CaB06fE2A485A31Cc49795C5C7aC500c698f3e4


## 🏄‍♂️ Quick start

Prerequisites: [Node](https://nodejs.org/en/download/) plus [Yarn](https://classic.yarnpkg.com/en/docs/install/) and [Git](https://git-scm.com/downloads)

#### 1. Clone repository

```bash
git clone https://github.com/selimerunkut/hibiscus_ethkl_hack2023
```

#### 2. Install and start your 👷‍ Hardhat chain:

```bash
cd hibiscus_ethkl_hack2023
yarn install
yarn chain
```

#### 3. In a second terminal window, start your 📱 frontend:

```bash
cd hibiscus_ethkl_hack2023
yarn start
```

Copy your local burner wallet address (top right)

#### 4. Deploy your contract:

In `packages/hardhat/deploy/00_deploy_your_contract.js` paste your wallet address:

```js
const TO_ADDRESS = "YOUR_FRONTEND_ADDRESS";
```

You can also tweak the script (add test data, etc)

In a third terminal window, run:

```bash
cd hibiscus_ethkl_hack2023
yarn deploy
```

#### 5. Run backend:

In a fourth terminal window, run the backend:

The project uses a local json file store as default.

You can switch to a Firebase (Firestore) data storage editing ```packages/backend/services/db.js```. You'll need to create a firebase project and download the service account key configuration in your computer and set an environment variable with the path to that file (```export GOOGLE_APPLICATION_CREDENTIALS="pathToServiceAccountKeyFile"```). You can generate and donwload the file in https://console.cloud.google.com/, under IAM & Admin > Service Accounts > Keys.

```bash
cd hibiscus_ethkl_hack2023
yarn backend
```

📱 Open http://localhost:3000 to see the app

### Semi-decentralized Budget Distribution

This build uses a Firebase data store for storing members and votes. The budget distribution creation and the votes are verified using signed messages. Then the budget distribution is done on-chain based on the information from the off-chain budget distribution.

## 📚 Documentation

 Documentation, tutorials, challenges, and many more resources, visit: [docs.scaffoldeth.io](https://docs.scaffoldeth.io)


## Special Thanks to

Code base: https://github.com/scaffold-eth/scaffold-eth/tree/qd-off-chain-voters-and-candidates

Built with [🏗 Scaffold-ETH](https://github.com/austintgriffith/scaffold-eth) as a [Moonshot collective](https://moonshotcollective.space/) project.