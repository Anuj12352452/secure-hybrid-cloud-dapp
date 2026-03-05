# Secure Cloud Data Sharing: A Hybrid Blockchain Access Model ☁️⛓️

An open-source prototype demonstrating how to combine **Decentralized Storage (IPFS)** with **Ethereum Smart Contracts** to build a secure, trustless, and GDPR-compliant cloud storage alternative. 

This project was developed as my MSc Data Science Applied Research Project at **York St John University (London Campus)**.

## 🚀 The Problem
[cite_start]Centralized cloud providers (AWS, Google Drive) operate as "Trusted Third Parties"[cite: 440]. This creates a single point of failure: if an administrator's credentials are compromised, millions of records are exposed. [cite_start]Furthermore, centralized logs can be tampered with, leaving users with no mathematical proof of who accessed their data[cite: 515, 518].

## 💡 The Solution (Hybrid Architecture)
This project removes the "Admin" entirely by orchestrating three layers:
1. [cite_start]**Security Layer (Client-Side AES-256):** Files are encrypted locally using Python before they ever leave the user's device[cite: 551].
2. [cite_start]**Storage Layer (IPFS/Pinata):** Heavy encrypted files are stored off-chain on the InterPlanetary File System, ensuring decentralized, high-availability storage without the massive gas costs of the blockchain[cite: 547].
3. [cite_start]**Access Control Layer (Ethereum):** A Solidity Smart Contract acts as the immutable "gatekeeper" on the Sepolia Testnet, maintaining the Access Control List (ACL) and creating a permanent audit trail[cite: 543, 544].

## ⚙️ Tech Stack
* [cite_start]**Smart Contracts:** Solidity (v0.8.0), Remix IDE [cite: 691, 693]
* [cite_start]**Backend Automation:** Python 3.10, Web3.py, Cryptography (Fernet AES-128/256) [cite: 695, 696]
* [cite_start]**Decentralized Storage:** IPFS, Pinata API [cite: 700]
* [cite_start]**Blockchain Network:** Ethereum Sepolia Public Testnet, MetaMask [cite: 689, 698]

## 🛡️ GDPR Compliance via "Crypto-Shredding"
[cite_start]A major challenge with blockchain is its immutability, which conflicts with the GDPR "Right to Erasure"[cite: 556]. [cite_start]This system solves this via **Crypto-Shredding**: by destroying the local decryption key, the encrypted off-chain data becomes mathematically unreadable forever, effectively satisfying erasure laws[cite: 558].

## 📊 Performance & Evaluation
* **Immutability:** Successfully eliminated the "mutable server log" vulnerability. [cite_start]Every access event is permanently stamped on Etherscan[cite: 844].
* [cite_start]**Gas Economics:** Uploading file metadata costs ~206,400 Gas (~$10.83 USD), and granting access costs ~48,700 Gas (~$2.55 USD)[cite: 864, 865, 871, 874]. [cite_start]While expensive for consumer use, it is highly viable for High-Value Data (Healthcare, Legal, IP)[cite: 879].
* [cite_start]**Latency:** Average block confirmation time of ~14 seconds on Sepolia[cite: 884]. 

## 🔮 Future Roadmap
* [cite_start]**Layer 2 Scaling:** Migrating contracts to Arbitrum or Optimism to reduce upload costs by ~95% (to <$0.10)[cite: 948].
* [cite_start]**Zero-Knowledge Proofs (zk-SNARKs):** Hiding user wallet addresses on-chain to ensure total privacy[cite: 955].

## 👨‍💻 About the Author
**Anuj Thakkar** MSc Data Science Graduate | London, UK  
