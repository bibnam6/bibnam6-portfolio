# 📘 Operator Logs - bibnam6

## ⛔ Terminated Project: Tanssi Network

**Status:** Node stopped and removed  
**Duration:** 2025-06-19 → 2025-06-23  
**Reason:** Operator role was only open to limited winners from Season 1. No rewards or onboarding for new participants.  
**Summary:**
- Successfully synced full node until final block
- Participated in Discord and submitted operator application
- Built full documentation and pitch on GitHub
- Closed due to lack of opportunity and no reward path

---

## 🆕 Active Project: CESS Network (Testnet)

**Status:** In Progress  
**Start Date:** 2025-06-23  

### ✅ Milestone 1: Initial Setup Complete

- Downloaded and extracted `cess-nodeadm v0.6.1`  
- Installed via `./install.sh`
- Switched to testnet profile: `cess profile testnet`
- Ran configuration: `cess config set`  
  - Mode: `storage`
  - Signature wallet: `cXkHLoDJiptaogn1uA435UVBT6vZwYb3xfVKeEcTVDD3LM1x4`
  - Disk: 300 GB
  - CPU: 8 cores (VPS full capacity)
- Started all services: `cess start`
- Verified containers running:
  - `chain`, `watchtower`, `autoheal`: **healthy**
  - `miner`: currently **unhealthy**

### 🛰️ Current Status

- Chain syncing at ~180 blocks/sec from height ~0 → ~4.4M
- 44+ peers connected
- Error logs show:
  - `audit: Select invalid miner`
  - `The measurement hash must be in SGX enviroment with "full_crypto"`  
  → Waiting for full sync before proceeding

### 🔜 Next Steps

- Confirm full sync via `docker logs -f chain`
- Register miner: `cess miner register`
- Verify on-chain status via Polkadot.js → `sminer` pallet
- Monitor health of miner container
- Attempt to receive delegation or TCESS airdrop for testnet staking
