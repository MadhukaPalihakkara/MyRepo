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

## c) Giveway. Move money to another Bitcoin wallet. Choose an amount where the last two digists are 42.

