# Bitcoin

### Table of Contents:
- [**Basics**](#1-basics)
  - [What is Bitcoin?](#11-what-is-bitcoin)
  - [How does Bitcoin work?](#12-how-does-bitcoin-work)
  - [What is Blockchain?](#13-what-is-blockchain)
  - [Full Nodes](#14-full-nodes)
  - [Proof of Work](#15-proof-of-work)
- [**Wallets**](#2-wallets)
  - [Types of Wallets](#21-type-of-wallets)
  - [Public Keys](#22-public-keys)
  - [Private Keys](#23-private-keys)
  - [Multisig Addresses](#24-multisig-addresses)
- [**Transactions**](#3-transactions)
  - [Send Bitcoin](#31-send-bitcoin)
  - [Receive Bitcoin](#32-receive-bitcoin)
  - [Network Fees (Miner Fees)](#33-network-fees-miners-feestransaction-fees)
- [**Mining**](#4-mining)
  - [Generating Bitcoin](#41-generating-bitcoin)
  - [Block Reward](#42-block-reward)
- [**Blockchain**](#5-blockchain)
  - [Blocks](#51-blocks)
  - [Block Height](#52-block-height)
  - [Block Size](#53-block-size)
- [**Forks**](#6-forks)
  - [Soft Forks](#61-soft-forks)
  - [Hard Forks](#62-hard-forks)
***

### 1. Basics
#### **1.1. What is Bitcoin?**
Bitcoin is a digital, peer-to-peer, decentralized payment system. It is the first cryptocurrency to be ever created.
- **Digital**: Bitcoin is not tangible. It just exists on the computer, unlike fiat currency (bills & coins).
- **Peer-to-Peer**: Bitcoin is sent directly from the Sender to Receiver. There is no third person involved in the transaction except for the Sender and Receiver.
- **Decentralized**: Bitcoin is not controlled by any central organization, be it a government or any financial regulator.
- **Cryptocurrency**: Bitcoin uses cryptography to sign, verify and broadcast transactions, hence it is called a cryptocurrency.

#### **1.2. How does Bitcoin Work?**
Bitcoin relies on a network of computers called _nodes_. When a transaction is created, the transaction is broadcast to all the nodes. Each node collects new transactions into a block. Each node works on finding a difficult proof-of-work for its block. When a node finds a proof-of-work, it broadcasts the block to all the nodes. Nodes accept the block only if all transactions in it are valid and not already spent. Nodes express their acceptance of the block by working on creating the next block in the chain, using the hash of the accepted block as the previous hash.

#### **1.3. What is Blockchain?**
Blockchain is a transaction database shared by all nodes in the bitcoin network. Blockchain contains a full copy of all the transactions ever executed on the Bitcoin network, stored in chronological order.

#### **1.4. Full Nodes**
A _node_ is any computer that connects to the bitcoin network. A _node_ that fully verifies all the rules of the Bitcoin protocol are known as **full nodes**. Practically, any computer running the **Bitcoin Core** wallet is a _full node_ as it downloads the complete blockchain before it is ready for use.

#### **1.5. Proof of Work**
A proof of work is a piece of data which is difficult (costly, time-consuming) to produce but easy for others to verify and which satisfies certain requirements. Producing a proof of work is usually a random trial and error process with very low probability of producing a valid result. For example, producing a block with a hash containing a certain number of zeroes is very tough computationally.


### 2. Wallets
A bitcoin wallet is a collection of public and its corresponding private keys.
#### **2.1. Type of Wallets**
Wallets are of different types depending on where they are stored.
- **Desktop Wallets**: These wallets are stored on a computer, and may be full nodes. Given the blockchain size (~130 GB at the time of writing), many prefer light bitcoin wallets. Some full desktop wallets include Bitcoin Core, Armory, etc. Light desktop wallets include Electrum, MultiBit, etc.
- **Hardware Wallets**: Hardware wallet is a special type of bitcoin wallet which stores the user's private keys in a secure hardware device. These provide an extra layer of security as they remain offline, and also, the private keys are stored in a protected area of a microcontroller, and cannot be transferred out of the device in plaintext. Ex: Trezor, Ledger Nano S, KeepKey, etc.
- **Mobile Wallets**: These wallets are stored on a mobile device. Depending upon the operating system of the mobile, the wallet apps vary. Ex: Coinomi, BitPay, etc.
- **Web Wallets**: Web wallets are the wallet services which facilitate storing the bitcoin private keys on the cloud. Usually the services do not offer the client a full control of his private keys. Ex: Coinbase, Blockchain.info Wallet, etc.

**AUTHOR'S NOTE**: Please avoid using web wallets and use desktop wallets, and if possible ,use hardware wallets. Web wallets are unsafe as they do not provide you full control over your private keys, and there is every chance they might shut down anytime.

#### **2.2. Public Keys**
- Public keys are the shareable part of the pubic-private key pair generated while creating a wallet.
- The public key is similar to an account number, to which the coins are to be sent to or to be received at.
- A bitcoin public key is usually 33-34 characters long and is Base58, and thus doesn't contain similar looking characters like `l` & `I` (small l & capital I), `0` and `O` (zero and the alphabet O), etc.
- A total of 2^160 public addresses are possible.
- A bitcoin address **always starts with `1`**, except for [_MultiSig addresses_](#Multisig-Addresses), **which start with `3`**.

#### **2.3. Private Keys**
- Private keys are the secret part of the public-private key pair generated while creating a wallet.
- These are required only to **spend the bitcoins** present in a public key, and thus **need to be kept confidential**.
- All **uncompressed private keys start with `5`**, and all **compressed private keys start with `K` or `L`**.
- Each public key has 2^96 possible private keys, but finding any two of them is nearly impossible computationally.

#### **2.4. Multisig Addresses**
- Multisig addresses require more than one signature to perform a **send** transaction.
- These are useful in situations where the coins in a public key are co-owned by two or more parties.
- Multisig bitcoin addresses **start with `3`**.


### 3. Transactions
#### **3.1. Send Bitcoin**
To send bitcoins, the sender needs to have the receiver's public key. Sending involves:
- Creating a transaction
- Signing the transaction with the sender's private key.
- Broadcasting the transaction to the nodes.
- Waiting for the transaction to receive confirmations from the network and to be included into a block.

Once the transaction is included into a block and has received confirmations, it is almost **irreversible**.

#### **3.2. Receive Bitcoin**
To receive bitcoins, you need to send the public key to the sender and ask for a payment to your address. You can also create a QR code containing the following text (URI):
```
bitcoin:<your_address_here>?amount=<insert_amount_here>
```

#### **3.3. Network Fees (Miners Fees/Transaction Fees)**
Network fees are the fees you pay to the miners to include your transaction into the block. This is mandatory and if appropriate fees aren't included, either the transaction confirmation is delayed, or if the fees is too low, the transaction is delayed indefinitely and is ultimately dropped from the network.


### 4. Mining
#### **4.1. Generating Bitcoin**
Miners solve complex and near impossible mathematics using their computation power (be is using ASIC, GPU or CPU) to mine a block, which is important for the survival of the bitcoin network. Every block contains a block reward which is the origin of the new bitcoins coming into circulation.

#### **4.2. Block Reward**
Block Reward is the incentive that miners receive for all the computation power they put in for mining a block. Presently, the block reward is `12.5 BTC`. This reward halves every 210,000 blocks (or approximately every 4 years). The reward was initially `50 BTC` which halved to `25 BTC` on `November 28, 2012`, and to `12.5 BTC` on `July 9, 2016`. The next halving will see the reward decrease to `6.25 BTC`.


### 5. Blockchain
#### **5.1. Blocks**
Blocks are files where data pertaining to the Bitcoin network is permanently recorded. A block records some or all of the most recent Bitcoin transactions that have not yet entered any prior blocks. Thus a block is like a page of a ledger or record book.

#### **5.2. Block Height**
Block height is the chronological number of the block last created, starting from 0 (Genesis Block).

#### **5.3. Block Size**
Block size is the size of the block in MB. The original proposal was `1 MB` per block, and it still continues to be the same today, but a lot of debate stirred when the blockchain network almost clogged in 2017. A lot of solutions were suggested like increasing the block size to `4 MB` or `8 MB`. The debate and different opinions of the developers gave rise to Hard Forks like Bitcoin Cash & Bitcoin Gold, and also paved the way to SegWit (Segregated Witness).


### 6. Forks
#### **6.1. Soft Forks**
Soft Forks are changes in the original source code of Bitcoin which was agreed upon by consensus. These forks do not give birth to a completely separate coin and a blockchain, unlike hard forks.

#### **6.2. Hard Forks**
Hard Forks are completely new branches originating from Bitcoin. These usually have differences in terms of the working principle. Bitcoin's hard forks include Bitcoin Cash (BCH), Bitcoin Gold (BTG), etc.
