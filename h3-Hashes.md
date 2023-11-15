# One-way has function 
## Book : Applied Cryptography: Protocols, Algorithms and Source Code in C, 20th Anniversary Edition
 
### Chapter 2.3
 
One-way function are relatively easy to compute but significantly harder to reverse.
For given X --> Easy to compute F(x), For given F(x) --> It is harder to compute X. 
Breaking a plate in to thousand pieces is the proper example, make it to the plate again a really difficult task.
 
What good are one-way functions?
We can't use them for encryption.
 
A trapdoor one-way function - 
Special type of One-way function with secret trap door. It is similar as one-way function but with the secret it is possible to easily compute the reverse way. 
For given X --> Easy to compute F(x), For given F(x) --> It is easier to compute X with the password y. 
 
### Chapter 2.4

A one-way hash function has many names: 
compression function, 
contraction function, 
message digest, 
fingerprint, 
cryptographic checksum, 
message integrity check (MIC), 
manipulation detection code (MDC).
 
Variable Length input --(Hash Function ) --> Fixed length output
 
Collision-free - It is hard to generate two pre images from same hash values. 
Function of the hash function is public; the security of the one-way has function of its one-wayness.
One-way hash function use in verification process:
Verify the file in two ends by sending the hash of the file
Verify the banking transactions by sending the hash of the withdrawal amount to verification process
 
Massage Authentication Code (MAC)  
Also known as Data Authentication Code (DAC)
A key is involving to the functionality and generate the hash using key and the input, but no reverse way of the process.
Special MAC functions available for this operation. 


# Cracking hashes with HashCat

Hashes are one way functions, this article shows how use HashCat to try out any matches against hashes of dictionary words.  
 
### Install HashCat
 
$ sudo apt-get update
$ sudo apt-get -y install hashid hashcat wget
 
 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/35e1b400-904b-4747-a35a-9b46dbbdae62)

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/f708f943-72d9-4837-bac3-f2dec421c445)

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/cce4ed39-e93c-48ed-aceb-563eaaf25a3d)

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/0ecfbbda-5306-4c7d-9624-fed360727367)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/577bc22a-1f84-48ad-9983-2167e1b7cd0f)
  
### Identify Hash type
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/15db8f6f-ae6a-45e0-a3e5-e6e59ee29c9a)

### Crack the Hash
 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/78a4e4e9-14a0-41b7-9516-6a3b5c4f55b8)

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/70312f00-a311-4b59-b840-84465d962dd2)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/a569386c-9f62-475e-91f2-9c251a316f65)

### Download the dictionary
$ wget https://github.com/danielmiessler/SecLists/raw/master/Passwords/Leaked-Databases/rockyou.txt.tar.gz
$ tar xf rockyou.txt.tar.gz
 
### Identify hash type
$ hashid -m 6b1628b016dff46e6fa35684be6acc96
 
 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/a5bb9e79-d8b7-4724-b974-b3ab1d3bcf83)

 According to the First 3 answers the hash would be MD2, MD5 or MD4. Since MD2 is no longer use, most suitable option would need to look at is MD5. 
 
### Test HashCat
 
Issue a HashCat command to crack the given hash. It is the MD5 hash of the work summer. 
 
 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/0b3f9064-40f8-4da2-91fd-037f7a0f1fed)

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/089e99b4-f882-466e-a688-8a3825e76aa6)

 
It is finally found the related word of the given hash and written it in to a text file using a given file name in the command "solved1.txt".
 
#	a) Billion dollar busywork
For small change in a input, complete hash value is changed. 
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/ec5dc03b-a265-4e7f-9339-c2001fe3ed36)

Get the Zero in front of the hash value : Keep trying with the various inputs and check the result has a leading zero. We can use a small script to check this out as shown in below. 
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/2c0440dd-a2c3-4fae-8f88-b937a0005ed1)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/600a0eec-e0d0-4a1c-9863-3564d641495b)

### How this related to BitCoin ?
Bitcoin mining is related to the same method. It finds hash values that has leading zeros. Number of leading zeros in next hashes are determined by the specific calculation in every two weeks' time. Currently miners finding next Bitcoin hashes with 17 leading zeros. Ever found lowest Bitcoin value has 23 leading zeros. 

### How many zeros can you get to the beginning?
 According to my opinion if enough computational power is available, theoretically it is possible to generate a hash with all zeros. 

# b)	Compare hashes

Create a file and get the hash

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/309d09b5-512e-41aa-89e1-bb1584f4af75)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/06730511-f113-4956-8104-6bd9da36cb0b)

Compare hashes 
First Hash : d2a84f4b8b650937ec8f73cd8be2c74add5a911ba64df27458ed8229da804a26
Second hash :  03ba204e50d126e4674c005e04d82e84c21366780af1f43bd54a37816b6ab340
 
Observation : Hashes are not equal or there are no any significant similarities. Completely different hashes were generated.
Conclusion : Any changes (even a small change) of the source file could generate a complete different hash values.  
 
# c)	Install a HashCat and test it work? 
   [Link to content above](https://github.com/MadhukaPalihakkara/MyRepo/blob/main/h3-Hashes.md#cracking-hashes-with-hashcat)

# d)	Crack this hash: 21232f297a57a5a743894a0e4a801fc3
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/cc4abd20-7881-4b58-88de-932765149420)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/330374d8-aac7-4b6d-b3f6-3fa3b7d41677)

Hash given hash is a MD5 hash and it was easily cracked with in milliseconds. The hashed words is admin.  

# e)	Creacked NTLM hash

Followig command use to crack the NTLM hash. 
Hash type 1000 (Using man pages)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/f8bb92d9-698c-4239-a596-c97d5d456921)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/206a9c57-fba6-4681-99bd-885bd376c13f)

The creacked password is monkey.

##	Try cracking this hash and comment on your hash rate $2y$18 $axMtQ4N8j/NQVItQJed9uORfsUK667RAWfycwFMtDBD6zAo1Se2eu .

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/ffa13ae9-c609-496f-a469-acfb37209abf)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/a68b6fea-9943-48fb-ad3e-80ed5f7b71b2)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/40ccf427-fd00-4618-b529-0e3eb587aaf5)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/c17ebd92-e032-4ea3-8e7f-b96b39959e23)

Speed Only option
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/c6ba36a1-ef2b-4a6f-88d6-074fbf41d192)

Command not provided the HashRate (Speed) because the given password was Cracked very easily. I checked the speed only command separately and the answer was same. 

# n)	create some hashes of your own, then crack them with hashcat

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/f5ade2be-09dd-4998-9dfa-2fc86a52496d)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/68510e6c-65b6-41b4-b690-59893cd10cb5)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/d9b43aa4-3d81-439e-9105-d3726744b034)

##	Cracking shs256 hash

Get the Sha256 hash

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/b1a21266-f031-41bd-8a5d-b04870dc61a3)

Get the hash id using hashhid command

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/b3813471-7188-4510-bb7b-87eb2c7ed3f1)

Crack the hash using HashCat but it was failed due to complexity of the hashed value.
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/c0f33d6b-9aca-44c5-8743-0cf71d6e15f6)

Information observed
Speed or HashRate is 2721.9 kH/s means 2721900 hashes processed per second. 
