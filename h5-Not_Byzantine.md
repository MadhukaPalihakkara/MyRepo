# Read and summarize 
## Nakamoto 2008: Bitcoin: A Peer-to-Peer Electronic Cash System
### 1 Introduction

•	The goal is to create a secure and direct method of online transactions while minimizing fraud.

•	Online transactions depend on trusted third-party financial institutions for payments.

•	These can lead to problems like transaction reversibility and increased costs.

•	This solution suggests an electronic payment system with cryptographic proof.

•	This allows direct transactions between two parties without a trusted third party.

•	The double-spending problem is solved with a timestamp server.

•	Honest users collectively have more computing power than potential attackers.

### 2 Transactions

•	This coin is like a chain of digital signatures.

•	Coin transfer by digitally signing the previous transaction's hash and the next owner's public key.

•	It is possible to verify the signatures to trace and validate the chain.

•	To verify double-spent the coin, the common solution is centralized authority or mint.

•	However, this relies on trusting the mint, like trusting a bank. Again, every transaction goes through the mint.

•	To ensure previous owners didn't sign earlier transactions without central authority, transactions must be publicly announced.

•	There should be a system to keep track of the order of the transactions, and most nodes agree on the transaction order.


### 3 Timestamp Server

•	A timestamp server takes a hash of a block of items to be timestamped and stamps on it.

•	Then hash is widely published.

•	Each timestamp includes the previous timestamp in its hash, forming a chain.

•	The chain of timestamps reinforcing the ones before it.


### 4 Proof-of-Work

•	In this timestamp network, proof-of-work is implemented by incrementing a nonce in the block until the hash meets the zero-bit requirement.

•	Proof-of-work solves representation issues in majority decision-making, ensuring one-CPU-one-vote instead of IP address.

•	The majority decision is represented by the longest chain.

•	Honest nodes control the majority of CPU power, making the honest chain grow the fastest.

•	To modify a past block, an attacker must redo the proof-of-work for that block and all subsequent blocks.

•	The difficulty of proof-of-work adjusts with a moving average targeting a set average number of blocks per hour.

### 5 Network

•	New transactions are sent to all nodes in the network, each node gathers these transactions into a block. 
Nodes then engage in finding a challenging proof-of-work for their block. 
Upon finding the proof-of-work, a node shares the block with all other nodes. 
Nodes only accept a block if its transactions are valid and not previously spent. 
To express acceptance, nodes start working on the next block, using the accepted block's hash as the previous hash.

•	The longest chain is always considered correct, and nodes continuously extend it.

•	If multiple versions are received, nodes work on the first one received but keep the other in case it becomes longer.

•	The tie is resolved when the next proof-of-work is found, making one branch longer, and nodes switch to the longer one.

•	Block broadcasts tolerate dropped messages.

### 6 Incentive

•	The first transaction in a block is special, creating a new coin for the block's creator.

•	This rewards nodes supporting the network and distributes coins without central authority.

•	Adding new coins is like gold miners adding gold to circulation; here, it's done by using CPU time and electricity.

•	The incentive can also come from transaction fees; the difference between input and output values adds to the block's incentive.

•	Once a set number of coins circulate, the incentive can shift entirely to transaction fees, making it inflation-free.

•	The incentive encourages nodes to stay honest by making it more profitable to follow the rules than to defraud the system.

•	If an attacker has more CPU power than honest nodes, they must choose between stealing payments or generating new coins, favoring the latter for greater profit.



## a) Wallet. Create a BitCoin testnet wallet.
![3](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/6ec24ad3-1dcf-4606-9887-ad60ccf10091)

![2](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/2062460f-a1f3-42ea-906f-f8baba41f084)

Note: wallet was created last week as inclass activity.

## b) Faucet. Get worthless fake money from a testnet Bitcoin faucet.

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/3247f2e6-fe3c-48cd-a73e-76fcb26afef1)

copy the address from here

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/445fb83c-71a0-46c7-b085-384e8cd5151e)

Got fake money not yet confirmed

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/7bf28686-80cd-4c4e-824e-ca7b3200c800)

Note: last two records are related to last week inclass activity 

Confirmed after sometime

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/80d6336a-940f-4908-8b43-7fd43bdbab6d)

## c) Giveway. Move money to another Bitcoin wallet. Choose an amount where the last two digists are 42.

Tried to send money 

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/c856aab9-f80b-4bff-9f7d-ca60b1ae5b9d)

but following error occured

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/f13670b0-0b49-4ecd-8ee8-e2b2197c66d0)

Then I close the window and reopen and tried again, it worked

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/37b2d5e9-57e1-422d-be6b-2ed4acbd73f8)

### d) Block Chain Explorer

Blockchain Explorers are powerful tools to give access to the real time and historical blockchain data. It also provide information about block heigh, difficulty, congestion and average transaction fees.  Alsi it provides details of Orphan blocks. 

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/aa5a1678-d733-4271-a0bc-c51a944fdf8c)

Explain what each value and field means.

Blocks :Number of confirmed Blocks, newest to oldest
Transactions: Number of transactions, newest to oldest
Outputs : Number of database rows represent traction outputs
Address : list of all addresses and their confirmed balances. 

Blockchain Size : Total size of all blocks and how its get increase over the time 
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/acbb9631-520e-483f-a1de-53e3d604f128)

Network nodes : Total nodes in the network. Nodes are devices authorized to keep track of the distributed ledger and serve as communication hubs for various network tasks

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/16d4da90-f90c-4ba7-93af-c4e758e53b65)

Block heights: Block height is a number of confirmed blocks in past form the initial block called Genesis block. As an example Genesis block height is zero and the next confirmed block height is  1. 
Last block : Adding new transaction to the block chain network means adding a block to the block chain as a last confirmed block.  It shows time and the block number. As an additional information hash of the block, block number and some other information related to the block available.
Difficulty :The extent of computational power needs mine a block is represented by the cryptocurrency difficulty.  

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/d3106135-5cc0-401c-8f40-1720fb0fe6bb)

Next estimated difficulty : Calculated difficulty for finding the next block. 
 
Next readjustment: Time to reset the difficulty level
 
Mempool :  Mempool indicate statistics of all the valid transactions waiting to be confirmed. High mempool traffic indicate more traffic and longer average conformation time and higher fees.  

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/e029179e-d2f6-444c-836a-054f8c53febb)

Finally explorer shows 24 hours statistics of the bitcoin blockchain transactions and price variation over the period of time.

Note: 
 
Orphan block - This is also known as stale or detached block. There are various factors involves cause an ophen block. Internet lags, length of the block chain, block size and the speed of the node in the block chain.   According to the factors above, it leads to generate two blocks with the same timestamp in two nodes and reject one of them when it attached to the main blockchain. For deciding which one should add to the main blockchain among two valid blocks, Bitcoin consider a block having a larger chain as a valid one. 


### Detailed a Trx

Explain what each value and field means.
 
1.	Get the sample transaction from the web 

  	a.	A1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d   (https://learnmeabitcoin.com/)

3.	Access Block explorer in Bitchair.com and provided the transaction id into the search box.

4.	It provides the following detailed information 

    a.	Trasaction Hash : a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d

  	b.	Amount transacted : 10,000.00 BTC

  	     The amount in USD at the time of transaction

5.	Transaction fee : 0,99 BTC

6.	Fee per vbyte : 4,191 Satoshi

7.	Date : 13 years ago (May 22, 2010 6.16 PM UTC)

8.	Transaction status : Confirmed

    a.	Confirmations: 761896

  	b.	Block id : 57,043

  	c.	Additional Info

   ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/539b9f31-43b2-4466-b050-4e5e24f12236)

  d. Sendors : 131
  
  e.	Recipient : 1
  
  f.	Sender current wallet statement
  
  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/61fac5fc-8a4c-4f0d-bd70-4a5ea867aed7)

  	


