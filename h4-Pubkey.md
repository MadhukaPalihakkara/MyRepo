# Read and summarize 

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

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/02083f0e-df71-483d-bca8-d2cdf5cf637b)

Alice can verify the same using fingerprint information

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/8341bf82-8a52-4f96-9ccf-3ce6e78fdf89)

Alice can add the fingerprint to manually

This is not worked due to some reason (To be check this again)

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/a8a3a812-3ada-4d63-819f-bfc58ad3a49f)

Alice send the secret message

## a)	 Explain how you have used public key cryptography today or yesterday
 
Every day, we access numerous websites to read emails, gather information, play games, and perform various other tasks. It is imperative for users to have trust in the websites they engage with. One commonly employed method for users to establish trust is by looking for the "https://" signature at the beginning of the URL.
 
The abbreviation "https" stands for Secure Hypertext Transfer Protocol, and it operates on the foundation of public key cryptography. It uses the SSL/TLS protocol for encryption and authentication. Https works on port 443 instead of famous unsecure default web port 80. 
 
HTTP was originally designed for plaintext communication, making it vulnerable to eavesdropping and man-in-the-middle attacks. To address these security concerns, SSL/TLS handshake protocols were introduced, enabling the transfer of encrypted messages between the client and server. This not only ensures confidentiality but also provides authentication and integrity, enhancing the overall trustworthiness of communication.
 
This security is primarily achieved through the use of public key certificates issued by a verified certificate authority for a specific website, domain, or IP address.
 
Browsers play a crucial role in enforcing this security measure by verifying the certificate before allowing users to access the content of a website. If the certificate is unknown, expired, or not signed by a trusted authority, browsers issue warnings to users, indicating potential unsecure communication.
 
Reference : The HTTPS-Only Standard - Introduction to HTTPS (cio.gov) , What is HTTPS? - SSL.com


## b)	Send an encrypted and signed message using PGP

## c)

## d)	Explain how PGP protects against Mallory and Eve

Protect against Eve : PGP utilizes public key cryptography to ensure the confidentiality of messages. The recipient's public key, which is publicly available, is used to encrypt the message, and only the recipient, possessing the corresponding private key, can decrypt it. The private key is confidential information known only to the recipient. If a message is encrypted with the public key, it can be decrypted only by the respective private key at the recipient's end, preventing eavesdroppers from extracting information as the message is encrypted.
 
However, there is a potential vulnerability. If the sender uses the wrong or compromised public key (set up by an attacker like Eve), the message could be read by the attacker. PGP addresses this issue by supporting the establishment of trust in the public key certificate through the verification of the signature on the public key. This ensures that Eve cannot compromise public keys during the initial phases of the encryption process.
 
Protect against Malloy : Instead of the original message, another attacker like Malloy could send a false message to the intended recipient, masquerading as the original sender. This is one of the exceptional use cases arising from tampering with communication methods. Malloy can achieve this in two ways: by modifying messages through intercepting the communication channel or by sending completely forged messages to the recipient. PGP addresses these security concerns by implementing preventive measures through the calculation of message and certificate signatures.
  
If Malloy alters only the message during transmission, the message signatures will fail verification at the recipient's end, allowing the detection of unintended modifications.
 
If Malloy changes both the message and the hash of the message, regeneration using the sender's public key becomes impossible because it was encrypted by the sender's private key.
 
In the scenario where Malloy sends a completely new message while pretending to be the original sender, the forged message signature cannot be extracted or verified using the sender's public key. Therefore, such attempts can be easily detected by the recipient. The protection remains effective as long as both the sender and recipient use the correct public key certificates.


## f)	Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers?

Password managers are small software applications designed to securely store our passwords. Typically, password managers require a single master password for access to the system, where other stored passwords can be retrieved. It is a good practice to keep passwords in a secure environment, such as a password manager, rather than writing them down on paper or storing them in an Excel file on your personal computer. Password managers play a crucial role in preventing various types of password theft, as outlined below.
 
Prevent using a weak password : Password managers enforce users to create passwords that comply with common complexity requirements or specific criteria set by the users. These tools also offer an auto-password generation option, freeing users from the need to formulate a new password themselves. Instead of manually coming up with a password, users can generate a new one by simply clicking a button in the graphical user interface (GUI). The password manager preserves the secrecy of the password by leveraging computational randomization power during the password generation process.
Common criteria's of secure password (refer : Password must meet complexity requirements | Microsoft Learn) .
NIST password standard 2022-2023  : NIST Special Publication 800-63B , NIST Password Best Practices: How to Keep Your Password Secure (psmpartners.com)
 
Secure password with compliance requirements : In addition to complexity, there are other requirements essential for maintaining secure passwords. Many security standards mandate these requirements as compulsory controls that must be adhered to. These standards are widely implemented globally, and a valuable resource for understanding these compliance requirements can be found at " Password Policy | Microsoft Learn". Password managers play a crucial role in tightly enforcing these requirements for passwords stored in their safes.
 
Alerting unsecure or compromised passwords: This is one of the latest features introduced by most password managers available today. It can verify the destination where users submit their credentials before utilizing them and prevents users from submitting information if the target is not secure. Furthermore, passwords are checked against a list of compromised passwords, and users are alerted to change their passwords immediately if a match is found (Ex : A breach alert feature available in Total Password tool).
 
Protect from losses: Forgetting and the loss of passwords are among the primary problems solved by password management tools. However, they remain vulnerable to various threats, including password database corruption, master key losses or forgetfulness, ransomware attacks, and device failures. It is highly advisable to perform regular backups of the key database file and maintain recovery keys (break the glass scenario) to prevent such losses. 
Protect from eavesdropping : When manually typing or copying passwords into a system, there is a high probability of them being traced by a nearby spy camera or an individual observing from behind. Password managers address this security concern by making the password entry process invisible when copying or modifying. This is a standard feature that comes with most password managers, enhancing the security of password usage. 
Protect form phishing attacks: Password managers keep track of stored URLs, allowing them to indicate to users whether the entered URL is valid or not. Reference :How password managers help prevent phishing | Bitwarden BlogL


## g) Done


