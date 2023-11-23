# Read and summarize 
## Schneier 2015: Applied Cryptography:
### 2.5 Communications Using Public-Key Cryptography

### 2.6 Digital Signatures




### 2.7 Digital Signatures With Encryption
### 2.8 Random And Pseudo-Random-Sequence Generation

## Rosenbaum 2019: Grokking Bitcoin
### Digital signatures 

•	Digital signature is a digital version of the handwritten signature.

•	Securing the content with a digital signature has three phases, which are preparation, signing and verification.

•	Private key and public key are a key pair, which can be used to encrypt and decrypt messages.

•	Encrypted by private key and decrypted by public key, is used as a digital signature implementation.

•	Encrypted by a public key and decrypted by a private key, is used as a way of secure communication.

•	A signature is an encrypted hash.

•	Keeping the private key secure is an individual responsibility.

•	Keeping the private key secure is challenging while knowing that if you lose the private key it will not be recovered or regenerated.

## Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg

GPG - Gnu privacy guard
 
Install PGP and related tools
 
 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/3b4e9083-bba7-4dc6-bc2e-5fc0e1f20eb1)

Pgp - Encryption tool

Micro - A Linux terminal based text editor that sits in-between vim and nano tools in terms of complexity

Psmisc - is a combination of small usable tools as describe below

    fuser  - reports the PIDs of processes that use the given files or filesystems.
    
    killall  - kills processes by name. It sends a signal to all processes running any of the given commands.
    
    Pidof  - reports the PIDs of the given programs. (Not this pidof program is used, however, but the one from Sysvinit.)
    
    Pstree -  displays running processes as a tree
    
### Create a key pair for Madhuka
 
A public and private key pair created with passphrase 

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/39c53162-c898-4db4-8f0d-5c6489a1691f)

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/8f3e0f8c-053c-4bec-b291-561f726affb2)

### Exchange the public key - Receiver (Key owner)

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/da58b15f-42e0-414f-9c19-754835a30855)

Important flags

 --armor - Only use ASCII, output can be viewed and copied.
 
Before send better to get confirm the type of the key by reading first few lines.

Note:

   base64 encoded
   
   End of the file marked as "-----END PGP PUBLIC KEY BLOCK-----" similar to the beginning of the file as shown below. 

  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/ea714888-1f2d-433f-b3ab-63a713370079)

  Create another user in the system called Alice and copy my public key to Alice's public folder

 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/9a95f83e-da6b-4d10-b077-6d17da9565d4)
 ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/392e789d-7771-431d-9be1-5a94f76380c7)

### Create keypair for Alice

Get another terminal and login as Alice using following command

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/5a75bf28-258c-4649-8e87-5649af6c784e)

Copy Maduka's public key in to safe location. (Ex: separate folder called AliceKeys ) 

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/91fc745b-dbee-49a1-980d-c57756cb4714)

Copy and renamed Madhuka's public key
 
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/08fd671c-811d-41e3-a1a1-0a686a104785)

Create new GPG settings for Alice 

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/27e61f5c-2d09-4af9-b971-9d247a2f78d3)

Create a key pair for Alice

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/a9d143f6-93fb-4211-9330-a8de27f927cd)
![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/557dd990-dd2d-40b0-8994-8535b82e6b5d)

See the fingerprints of the created information 

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/dc789fed-2fa5-41f3-97a8-5d714b57d1a9)

### Use Madhuka's public key

Import Madhuka's public key

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/e4e0b6cc-a1a3-4d39-b8c7-92387726a4fa)

Verify Madhuka's public key

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/70182d74-9d5d-4ce5-847a-483da2102d43)

Get the Madhuka's signature of the public key offline, because it not trusted at this point. To make it trusted, Alice needs to manually verify it as follows.

Get the signature from Madhuka

   Note : Madhuka has to generate the key using the command below and share it with Alice.




## a)

## b)

## c)

## d)

## f)

## g)

## h)
