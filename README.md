# Bitcoin Scripting Assignment

**Assignment 3: Bitcoin Scripting**  

## Team Members:
- **Janapareddy Vidya Varshini** - Roll No:230041013
- **Korubilli Vaishnavi** - Roll No: 230041016
- **Mullapudi Namaswi** - Roll No:230041023


## Overview  
This project demonstrates the creation and validation of Bitcoin transactions using:

Legacy (P2PKH) Transactions

SegWit (P2SH-P2WPKH) Transactions

We use Bitcoin Core (bitcoind) in regtest mode and Python scripts to interact with it via RPC calls. The project includes:

Setting up a Bitcoin regtest network.

Creating wallets and generating addresses.

Funding transactions and analyzing scripts.

Comparing transaction sizes between Legacy and SegWit formats.
## Features  
- Connect to `bitcoind` using RPC  
- Create and load a Bitcoin wallet  
- Generate three **legacy addresses** (A, B, and C)  
- **Fund Address A** by mining blocks  
- **Create and sign a transaction** from A → B → C  
- Decode transactions and extract **locking (ScriptPubKey) and unlocking (ScriptSig) scripts**  
- Analyze and validate Bitcoin scripts  

## Requirements  
Ensure you have the following installed:  
1. **Bitcoin Core** (bitcoind)  
2. **Python 3**  
3. **Dependencies:**  
