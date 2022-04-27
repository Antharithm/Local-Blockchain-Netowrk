# POA-Private-Blockchain-Network
A private Blockchain testnet for a developer team to use and explore the potentials of blockchain technology at ZBank.
---
### Backround:
---
ZBank is a small, innovative bank that is interested in exploring what blockchain technology can do for them and their customers.

The goal of this project was to set up a private blockchain testnet for the developer team at Zbank so they can explore the potentials of this technology.

I loaded the testnet accounts with fake Ethereum which can be used for transactions and behave just like real Ethereum would on mainnet. This will give our team of developers the freedom to experiment and get used to the process of sending and receiving transactions.

Tokens inherently have no value in a testnet environment, so we will provide pre-configured accounts and "nodes" for an easy setup. Below is the documentation for other developers on how to start using the pre-configured nodes and accounts that I built for launching a private blockchain.

### Preliminary Steps - Installing dependencies and environment configuration:
---
Download the Blockchain tools (Geth & Tools): https://geth.ethereum.org/downloads/
This package includes the software to manage blockchain

Download MyCrypto:https://download.mycrypto.com/
Use MyCrypto GUI Wallet to connect to blockchain and make transactions

Use Git Bash (Windows) / Terminal (Mac) to navigate to the directory containing Blockchain tools

### Local Blockchain Setup
---
### Create the Genesis Block: Create a local network and Genesis Block using this command: 

./puppeth

![Puppeth_Config](https://user-images.githubusercontent.com/83500098/137602768-937284e9-40f1-44a9-9ead-1fda63f80f19.PNG)
---
### Next, initialize the two local nodes using these commands:

NODE1:

./geth --datadir node1 init zbanksnet.json

![Initialize_Node1](https://user-images.githubusercontent.com/83500098/137602822-a65654b6-9297-4b2f-b7cc-f6ffe80e6241.PNG)

NODE2: (open a second terminal, navigate to the directory where both nodes are saved)

./geth --datadir node1 init zbanksnet.json

![Initialize_Node2](https://user-images.githubusercontent.com/83500098/137602831-ecf46d7b-6a52-4002-bcb6-afda2c5e1a23.PNG)
---
### Unlock nodes and start mining blocks with these commands:

./geth --datadir node1 --unlock "node1_public_account" --mine --rpc --allow-insecure-unlock

./geth --datadir node2 --unlock "node2_public_account" --mine --port 30304 --bootnodes "enode://NODE1_ENODE" --ipcdisable --allow-insecure-unlock

![Enode](https://user-images.githubusercontent.com/83500098/137603013-56693fc7-5129-4de4-8832-dbbce0c216f0.PNG)
---
### Launch MyCrypto wallet and setup the custom node connection:

![Show_Custom_Node](https://user-images.githubusercontent.com/83500098/137603047-e8c5a195-0351-4e7b-95a4-80ad2d7d5687.PNG)
---
### Unlock node1 account with the keystore file:

![Unlock_Account_Keystore_file](https://user-images.githubusercontent.com/83500098/137603058-5bf2866d-166e-4f7e-8a5f-7d506990af50.PNG)
---
### Send testnet Ethereum to node2 account:.

![Sent_ETH_to_Node2_and_Tx_Status](https://user-images.githubusercontent.com/83500098/137603083-c2ec839e-a000-46c8-87cc-7d6c91594f86.PNG)
---
### DONE!
