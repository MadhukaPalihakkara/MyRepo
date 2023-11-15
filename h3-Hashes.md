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


