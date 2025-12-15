# Smart Contract Lottery 🎟️

A **decentralized lottery (raffle)** built with **Solidity** using **Foundry**. The contract allows users to enter the lottery by paying an entrance fee. After a fixed time interval, a **random winner** is selected using **Chainlink VRF**, and the prize pool is transferred automatically.

---

## ✨ Features

* Fully decentralized lottery
* Provably fair randomness via **Chainlink VRF**
* Automated winner selection
* Time-based lottery rounds
* Secure and gas-efficient Solidity code
* Unit & integration tests with Foundry

---

## 🛠 Tech Stack

* **Solidity** (^0.8.x)
* **Foundry** (Forge & Cast)
* **Chainlink VRF** (Verifiable Random Function)
* **Chainlink Automation** (Upkeep)

---

## 📂 Project Structure

```
smart-contract-lottery/
├── src/
│   └── Raffle.sol
├── script/
│   └── DeployRaffle.s.sol
├── test/
│   └── RaffleTest.t.sol
├── lib/
│   └── forge-std
└── README.md
```

---

## ⚙️ How It Works

1. Users enter the lottery by sending ETH greater than or equal to the **entrance fee**.
2. Entries are stored until the **time interval** passes.
3. Chainlink Automation checks if conditions are met.
4. Chainlink VRF generates a **random number**.
5. A winner is selected randomly.
6. The total balance is transferred to the winner.

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone <repo-url>
cd smart-contract-lottery
```

### 2️⃣ Install Dependencies

```bash
forge install
```

### 3️⃣ Compile

```bash
forge build
```

### 4️⃣ Run Tests

```bash
forge test
```

---

## 🔐 Environment Variables

Create a `.env` file and add:

```
PRIVATE_KEY=your_private_key
RPC_URL=your_rpc_url
CHAINLINK_VRF_COORDINATOR=address
SUBSCRIPTION_ID=your_subscription_id
GAS_LANE=key_hash
CALLBACK_GAS_LIMIT=500000
```

---

## 🧪 Testing

* Unit tests for entering raffle
* Revert tests for invalid states
* Winner selection tests
* Event emission checks

All tests are written using
