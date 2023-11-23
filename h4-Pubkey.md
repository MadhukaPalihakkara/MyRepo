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
 


## a)

## b)

## c)

## d)

## f)

## g)

## h)
