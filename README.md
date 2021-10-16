# POA-Private-Blockchain
A private Blockchain testnet for a developer team to use and explore the potentials for blockchain technology at ZBank.
---
### Backround:
---
ZBank is a small, innovative bank that is interested in exploring what blockchain technology can do for them and their customers.

The goal of this project was to set up a private blockchain testnet for the developer team at Zbank so they can explore the potentials of this technology.

I loaded the testnet accounts with fake Ethereum which can be used for transactions and behave just like real Ethereum would on mainnet. This will give our team of developers the freedom to experiment and get used to the process of sending and receiving transactions.

Tokens inherently have no value in a testnet environment, so we will provide pre-configured accounts and "nodes" for an easy setup. Below is the documentation for other developers on how to start using the pre-configured nodes and accounts that I built.

### Preliminary Steps - Installing dependencies and environment configuration:
---
Download the Blockchain tools (Geth & Tools): https://geth.ethereum.org/downloads/
This package includes the software to manage blockchain

Download MyCrypto:https://download.mycrypto.com/
Use MyCrypto GUI Wallet to connect to blockchain and make transactions

Use Git Bash (Windows) / Terminal (Mac) to navigate to the directory containing Blockchain tools

### Local Blockchain Setup
---
Create the Genesis Block: Create a local network and Genesis Block using this command: 

./puppeth

![Puppeth_Config](https://user-images.githubusercontent.com/83500098/137602768-937284e9-40f1-44a9-9ead-1fda63f80f19.PNG)
---
Next, Create two local nodes using these commands:

NODE1:

./geth account new --datadir node1

![Initialize_Node1](https://user-images.githubusercontent.com/83500098/137602822-a65654b6-9297-4b2f-b7cc-f6ffe80e6241.PNG)

NODE2:

./geth account new --datadir node2

![Initialize_Node2](https://user-images.githubusercontent.com/83500098/137602831-ecf46d7b-6a52-4002-bcb6-afda2c5e1a23.PNG)

