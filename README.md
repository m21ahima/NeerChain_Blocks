# ⛓️ NeerChain — Python Blocks

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
🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊
   NEERCHAIN — BLOCKCHAIN + MERKLE TREE DEMO
🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊🌊
🌊 NeerChain — Blockchain Initialized
Creating Genesis Block...

⛏️  Mining Block #0...
✅ Block #0 mined! Nonce: 288
   Hash: 00c7d4855285145b9665bf672310154ff86785f85bf4cb70aca4b0a4f9c5aa01

📦 Adding water safety readings to blockchain...

⛏️  Mining Block #1...
✅ Block #1 mined! Nonce: 26
   Hash: 001e63daf74f860d2cf5ab94a27f328464594177d21e65557fe4edce4282b047

⛏️  Mining Block #2...
✅ Block #2 mined! Nonce: 128
   Hash: 00e392a9f200fb621a9da1664dc6139a29c84b3013b4c37bc9db2ccef3a6c9c3

⛏️  Mining Block #3...
✅ Block #3 mined! Nonce: 283
   Hash: 00f473bc3e67061e9289b684214fb3b058828c6432aac605baa77c3b8b8f559c

⛏️  Mining Block #4...
✅ Block #4 mined! Nonce: 166
   Hash: 008725ad0ac28260974ea3e8cb44e0d73b44af2ce94386f442d872bb9ac5cb01

============================================================
  🔗 NEERCHAIN — FULL BLOCKCHAIN
============================================================

============================================================
  BLOCK #0
============================================================
  Timestamp   : 2026-03-23 15:12:59
  Data        : Genesis Block — NeerChain Water Safety
  Nonce       : 288
  Prev Hash   : 0...
  Hash        : 00c7d4855285145b9665bf67231015...
============================================================

============================================================
  BLOCK #1
============================================================
  Timestamp   : 2026-03-23 15:12:59
  Data        : {"city": "Vijayawada", "pH": 4.8, "turbidity": 7.5, "TDS": 620, "DO": 3.2, "status": "CRITICAL", "signature": "CHEMICAL_DUMP", "confidence": "99%", "action": "WATER_SUPPLY_FLAGGED", "authority": "CPCB + District_Collector"}
  Nonce       : 26
  Prev Hash   : 00c7d4855285145b9665bf67231015...
  Hash        : 001e63daf74f860d2cf5ab94a27f32...
============================================================

============================================================
  BLOCK #2
============================================================
  Timestamp   : 2026-03-23 15:12:59
  Data        : {"city": "Guntur", "pH": 7.2, "turbidity": 2.1, "TDS": 310, "DO": 7.8, "status": "SAFE", "signature": "NONE", "confidence": "95%", "action": "READING_LOGGED", "authority": "NONE"}
  Nonce       : 128
  Prev Hash   : 001e63daf74f860d2cf5ab94a27f32...
  Hash        : 00e392a9f200fb621a9da1664dc613...
============================================================

============================================================
  BLOCK #3
============================================================
  Timestamp   : 2026-03-23 15:12:59
  Data        : {"city": "Rajahmundry", "pH": 5.1, "turbidity": 6.8, "TDS": 480, "DO": 4.5, "status": "ALERT", "signature": "INDUSTRIAL_RUNOFF", "confidence": "87%", "action": "WARNING_ISSUED", "authority": "Municipal_Water_Authority"}
  Nonce       : 283
  Prev Hash   : 00e392a9f200fb621a9da1664dc613...
  Hash        : 00f473bc3e67061e9289b684214fb3...
============================================================

============================================================
  BLOCK #4
============================================================
  Timestamp   : 2026-03-23 15:12:59
  Data        : {"city": "Visakhapatnam", "pH": 9.2, "turbidity": 3.5, "TDS": 420, "DO": 5.8, "status": "ALERT", "signature": "ALKALINE_POLLUTION", "confidence": "78%", "action": "WARNING_ISSUED", "authority": "Municipal_Water_Authority"}
  Nonce       : 166
  Prev Hash   : 00f473bc3e67061e9289b684214fb3...
  Hash        : 008725ad0ac28260974ea3e8cb44e0...
============================================================

============================================================
  📊 BLOCKCHAIN SUMMARY
============================================================
  Total Blocks : 5
  Difficulty   : 2
  Chain Valid  : ✅ Yes
============================================================


🌿 Building Merkle Tree from transactions...

============================================================
  🌿 MERKLE TREE — NeerChain
============================================================

  📋 Leaf Nodes (Transaction Hashes):
  TX1: TX1: Vijayawada | CRITICAL | CHEMICAL_DU...
       Hash: 2a7b26022093ec73ccf9a0b7045a29...
  TX2: TX2: Guntur | SAFE | NONE...
       Hash: 1b086326406530fd63ca8412c7e6dd...
  TX3: TX3: Rajahmundry | ALERT | INDUSTRIAL_RU...
       Hash: 794818fdbf7ec446e9baee0c215681...
  TX4: TX4: Visakhapatnam | ALERT | ALKALINE_PO...
       Hash: 897a4a59fa5b9bdcf0a330c2e4c820...

  Level 1 nodes:
  Hash(2a7b26022093ec7... + 1b086326406530f...)
  = 3e95c0d1c760df83de9a157927cb5f...
  Hash(794818fdbf7ec44... + 897a4a59fa5b9bd...)
  = e8df27b2fcd3caa702df0873d85837...

  Level 2 nodes:
  Hash(3e95c0d1c760df8... + e8df27b2fcd3caa...)
  = edaf9f3d01c0cea8c46f4b82336c5d...

  🌳 MERKLE ROOT:
  edaf9f3d01c0cea8c46f4b82336c5d87871a8e408d5d9af1f0f239831b9cc628
============================================================

✅ COMPLETE!
   Blockchain blocks: 5
   Merkle root: edaf9f3d01c0cea8c46f4b82336c5d...
   Chain valid: True
```

## 🔗 Related Repos

- [NeerChain DApp](https://github.com/m21ahima/NeerChainDapp) — Full Blockchain DApp with Ganache + MetaMask
