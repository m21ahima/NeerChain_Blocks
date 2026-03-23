# ⛓️ NeerChain — Python Blockchain & Merkle Tree

Python implementation of blockchain concepts for the NeerChain Water Safety project.

## 🚀 What It Does

- Creates a blockchain with Genesis block + 4 water safety blocks
- Each block contains real NeerChain water quality transaction data
- SHA-256 hashing links blocks together
- Proof-of-Work mining with nonce generation
- Chain validation to detect tampering
- Merkle Tree built from all transactions

## 📦 Requirements
```bash
pip install hashlib
```
(hashlib is built into Python — no installation needed!)

## ▶️ How to Run
```bash
python blockchain_blocks.py
```

## 📋 Sample Output
```
🌊 NeerChain — Blockchain Initialized

⛏️  Mining Block #1...
✅ Block #1 mined! Nonce: 358
   Hash: 007b883136fd60e3...

⛏️  Mining Block #2...
✅ Block #2 mined! Nonce: 215

🌿 MERKLE TREE — NeerChain
   TX1: Vijayawada | CRITICAL | CHEMICAL_DUMP
   TX2: Guntur | SAFE | NONE
   ...
   🌳 MERKLE ROOT: edaf9f3d01c0cea8...

✅ Chain valid: True
```

## 🔗 Related Repos

- [NeerChain DApp](https://github.com/m21ahima/NeerChainDapp) — Full Blockchain DApp with Ganache + MetaMask
