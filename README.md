# **Time-Locked Liquidity Smart Contract**

## **📝 Description**
Time-Locked Liquidity is a Move-based smart contract deployed on the Aptos blockchain. It allows users to deposit Aptos Coins (APT) into a liquidity pool with a predefined lock period. Funds can only be withdrawn after the lock period has expired, ensuring a secure and transparent time-based liquidity management system.

---

## **🎯 Vision**
The primary goal of this contract is to:
- Enable trustless liquidity locking for projects and individuals.
- Prevent early withdrawals to maintain financial discipline.
- Provide a transparent and secure mechanism for time-bound asset holding.

---

## **🚀 Future Scope**
This project aims to evolve with:
1. **Multi-Currency Support** - Extending liquidity locking to various tokens beyond Aptos Coin.
2. **Staking & Rewards Mechanism** - Offering incentives for users who lock their funds for longer periods.
3. **NFT-Based Liquidity Locking** - Allowing NFTs to represent locked assets.
4. **Governance Features** - Introducing a DAO-based decision-making system for unlocking funds under special conditions.
5. **UI/Frontend Integration** - Creating a user-friendly dApp interface for seamless interaction.

---

## **📜 Contract Details**

### **1️⃣ LiquidityPool Structure**
The contract defines a **LiquidityPool** structure to store:
- **owner**: Address of the user locking the funds.
- **amount**: The number of tokens locked.
- **unlock_time**: Timestamp when funds can be withdrawn.

```move
struct LiquidityPool has store, key {
    owner: address,
    amount: u64,
    unlock_time: u64,
}
```

### **2️⃣ Functions**

#### **🔹 create_pool(owner: &signer, amount: u64, lock_duration: u64)**
- Creates a new liquidity pool.
- Withdraws `amount` of Aptos Coins from the user's wallet.
- Locks the funds for the specified `lock_duration`.

#### **🔹 withdraw_funds(owner: &signer)**
- Allows withdrawal of locked funds after the `unlock_time` has passed.
- Ensures funds cannot be withdrawn early.
- Returns the deposited amount to the original owner.

---

## **📦 Deployment & Usage**
### **🔧 Compilation**
To compile the contract, run:
```sh
aptos move compile
```

### **🚀 Deploying the Smart Contract**
```sh
aptos move publish --profile default
```

### **🔑 Interacting with the Contract**
Use Aptos CLI or a frontend dApp to interact with the contract:
- Call `create_pool` to lock funds.
- Call `withdraw_funds` to retrieve locked funds after the unlock period.

---

## **🛠️ Contributing**
Contributions and suggestions are welcome! Open a pull request or reach out with any feature requests.

---
## **Contract address**
0xd27954a610f78136e77a6c5ccaf7540ed243dfe1e8c7a3e1def65ee4a7b3c8d2
![Screenshot 2025-03-26 100914](https://github.com/user-attachments/assets/47313ac9-38bb-4f00-ad5c-ae107f343f6c)


