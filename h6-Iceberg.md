# x) Read and summarize 

## Shavers & Bair 2016: Hiding Behind the Keyboard: The Tor Browser

### Introduction

•	Tore is a browser that can anonymously browse the internet

•	Anyone can user this without technical instructions

•	Free to download and simple to use 

•	Tore hides the originating IP when surfing the websites

### History and Intended Use of The Onion Router

•	Initially developed by the US government in 2002, presently not controlled by any single entity but open for improvements and test 

•	Tore intended to anonymously communicate through the internet


### How The Onion Router Works

•	Tor Routing Process directs user's Internet traffic through random relays on the Internet.

•	At the start data is encrypted with elliptic curve cryptography, which is like a strong layer of protection.

•	Then, it goes through three stops, entry, middle, and exit relays. At each stop, one layer of protection is taken off. 

•	Finally, at the exit relay, the data connects to its destination without the extra layers,

•	Exit relay is only aware of the last previous node and nothing about traffic route.

•	And the route change entry, middle, and exit relays every 10 minutes.

###  Tracking Criminals Using TOR

•	FBI once broke Tore, using an exploit of Firefox.

•	Tore is safe with its default settings; customizations are not recommended. Eg- Geolocations, plugins, scripts.

•	There are number of ways that researchers use t break Tor, some are 

      o	disrupting a significant portion of the Tor network
      o	gaining control of entry and exit nodes to correlate traffic and identify users
      o	Man-in-the-middle attacks
      o	Emails or documents with IP address tracking code
      o	identifying the Tor user outside of the Tor network
      
•	there are several cases detected not because of vulnerabilities of Tore but mistakes made by users.

## Quintin 2014: 7 Things You Should Know About Tor

•	Tore has not broken and the best attacks on Tore so far are vulnerabilities of browsers, configuration issues or traffic correlation attacks. 

•	Tore has more value than supporting criminals, like whoever seeks privacy like military for secure communications and planning, families for privacy, and journalists for their researchers and secure communication with sources. 

•	Tore is dedicated to privacy and anonymity, cryptographers and security professionals confirm there is no backdoor.

•	Running a Tor relay is not illegal in US.

•	Tor is easy to use, download the Tore browser bundle and start use with secure pre-configurations. Tor can also be used with live OS like Tails.

•	Tor is slower than a regular browser, but it can be speed up by creating more relays.

•	To get the benefit of Tore users have to use it correctly.


## a) Install TOR browser and access TOR network (

1. Download the Tor browser package
### https://www.torproject.org/download/

2. Verify the signature
   
Copy signature file and the downloaded file to a local folder Documents named Tor
  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/f5a9fa72-51f5-4385-96c6-f9a32d33295b)

Get the developers public key that use to sign the Tor browser distribution and import it to GnuPg

  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/c2c813fa-3f52-4c4b-9eac-acb6edee0c68)

Save the imported key in to a file named tor.keyring in the same folder

  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/c25fbfe7-5c13-4b77-ade5-b921ddba4016)

Verify the signature 

Signature has been verified as a valid signature. Therefor we can ensure the trustworthiness of the package downloaded from the internet. 

  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/2275e504-c0d0-46b1-bceb-2df6b425b46d)

3. Extract the archive 

  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/10df46d3-ff09-4727-a154-fda1bf771cc2)

  Extracting files and finally created an new directory named tor-browser.

  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/2b7c7eaa-017c-4264-b53c-5b9d96503395)

4. Now Tor Browser can be run by executing the start-tor-browser.desktop file available inside the folder

  a. File was not executed due to a permission issue as follows
   
  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/12e920e3-b801-403f-aae0-0c006867008e)

  b. File  permissions and owner need to be changed in order to fix this error. Set the executable flg-on inorder to start-tor-browser file.

   ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/9290a613-dd91-4bba-870b-60d39afa72e1)

Owner and group information changed from root to Madhuka 

  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/cfb968e2-c171-42f5-ae2a-00e20a7c7a33)

5. Open the browser
   
  a. The following options are available to register the browser and run the browser.
  
  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/69c7d8a5-38eb-41e4-abd1-a9b78edb8849)

Note: Tor Browser application not allowed to run as root user. Instead, run it as a normal user as shown in the second command above. The Tor Browser is registered as an application.  

  b. Start Tor Browser
      
  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/ed530a6b-7bac-4b45-87cb-badf1970b43d)

  ![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/9afd77d3-a7ca-42a1-93a4-0f8be513007b)

### Connect to the network and check my publicly visible IP address

From normal browser - country is Finland

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/94e0445e-a787-4f23-a73d-a556784a7f14)

From Tor Browser - country shows as Nigeria

![image](https://github.com/MadhukaPalihakkara/MyRepo/assets/149093784/e72752fe-3faf-4c45-830b-abadbbc6bbe1)


## b) Browse TOR network, find, take screenshots and comment

#### search engine for onion sites

#### marketplace

#### fraud

#### forum

#### a well known organization

## c) In your own words, how does anonymity work in TOR? 

Tor guides the internet traffic through random points (relays) on the internet, before sending there will be layers of strong encryption along the way. Each point peels off one layer of encryption until the final point (exit relay) connects to the intended destination without encryption. Tor makes it hard to trace by changing the starting, middle, and ending points of the internet route every 10 minutes. So it is not easy to track IP addresses which will provide anonimity. 

## d) What kind of the threat models could TOR fit? 

## References


