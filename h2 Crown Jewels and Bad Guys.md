# Read and summarize
## Hutchins et al 2011
### Summary
 
Intelligence-driven computer network defense is a risk management strategy that addresses the threat component of risk, incorporating analysis of adversaries, their capabilities, objectives, doctrine, and limitations. This is necessarily a continuous process, leveraging indicators to discover new activity with yet more indicators to leverage.
 
APT actors, by their nature, attempt intrusion after intrusion, adjusting their operations based on the success or failure of each attempt.
 
In a kill chain model, just one mitigation breaks the chain and thwarts the adversary, therefore any repetition by the adversary is a liability that defenders must recognize and leverage.
 
U.S. military targeting doctrine defines the steps of this process as find, fix, track, target, engage, assess (F2T2EA).
Expanding on this concept, this paper presents a new kill chain model,one specifically for intrusions.
The intrusion kill chain is defined as reconnaissance, weaponization, delivery, exploitation, installation, command and control (C2), and actions on objectives.
 
1.	Reconnaissance - Research of targets. (Internet websites, mailing lists, social relationships, Technologies, etc)
2.	Weaponization - Coupling a remote access trojan with an exploit into a deliverable payload. (PDF, Word, etc)
3.	Delivery - Transmission of the weapon to the targeted environment. (Email, Web Downloads, USB)
4.	Exploitation - exploitation triggers intruders’ code. (Auto execute code, by user intervention)
5.	Installation - Installation of a remote access trojan or backdoor
6.	Command and Control (C2)  - establish a outbound C2 channel.
7.	Actions on Objectives - After six of above successful actions, take the final action to achieve their original objectives. (data exfiltration, violations)
 
The conventional incident response process initiates after our exploit phase, illustrating the self-fulfilling prophecy that defenders are inherently disadvantaged and inevitably too late. Defenders must be able to move their detection and analysis up the kill chain and more importantly to implement courses of actions across the kill chain. Defenders must collect as much information on the mitigated intrusion as possible, so that they may synthesize what might have happened should future intrusions circumvent the currently effective protections and detections
 
For example, if a targeted malicious email is blocked due to re-use of a known indicator, synthesis of the remaining kill chain might reveal a new exploit or backdoor contained therein. Without this knowledge, future intrusions, delivered by different means, may go undetected.
 
The principle goal of campaign analysis is to determine the patterns and behaviours of the intruders, their tactics, techniques, and procedures (TTP), to detect “how” they operate rather than specifically “what” they do.
The defender’s objective is less to positively attribute the identity of the intruders than to evaluate their capabilities, doctrine, objectives and limitations; intruder attribution, however, may well be a side product of this level of analysis
As defenders study new intrusion activity, they will either link it to existing campaigns or perhaps identify a brand new set of behaviors of a theretofore unknown threat and track it as a new campaign.
 
Another core objective of campaign analysis is to understand the intruders’ intent. This necessitates trending intrusions over time to evaluate targeting patterns and closely examining any data exfiltrated by the intruders.
 
 
### What does it mean to me :
 
The kill chain represents a new process that has evolved from enhancing the existing F2T2EA model, addressing certain missing components related to intrusion detection perspectives. 
Traditional intrusion detection methodologies typically focus on identifying intrusions post the exploitation phase in the new model. However, this document underscores the importance of analyzing the entire attack path to comprehend the behaviors associated with the attack and prevent more sophisticated forms of attacks, such as Advanced Persistent Threats (APTs). Examining adversaries based on the seven-phase model proposed in this document enables defenders to implement more effective precautions in the early stages of the attack lifecycle at minimal cost. Ultimately, this article highlights the significance of analyzing and correlating attacks to gain valuable insights for the easy detection and prevention of subsequent, zero-day, and future attacks. It is often observed that certain common indicators persist across previous adversaries, even as new ones attempt to remain undetected.

## Threat Model
### Summary
Threat model is a way to anticipate the threats that could affect you. begin threat modeling by focusing on four key questions:
What are you building?
What can go wrong?
What should you do about those things that can go wrong?
Did you do a decent job of analysis?

you should draw trust boundaries wherever different people control different things. Such as 

•	Accounts (UIDs on unix systems, or SIDS on Windows)

•	Network interfaces

•	Different physical computers

•	Virtual machines

•	Organizational boundaries

•	Almost anywhere you can argue for different privileges

Think about threat model diagrams as part of the development process, so try to keep it in source control with everything else.

Using STRIDE (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, and Elevation of Privilege) as a mnemonic can help you walk through a diagram and select example threats. Pair that with a little knowledge of security and the right techniques, and you'll find the important threats faster and more reliably. 

The next step in the threat modeling process is to go through the lists and address each threat. Actions would be Mitigate it, eliminate it, transfer it, or accept it.

Validation of your threat model is the last thing you do as part of threat modeling. You should ensure that the final model matches what you built. Answering following questions will ease the validation.

•	Is this complete?

•	Is it accurate?

•	Does it cover all the security decisions we made?

•	Can I start the next version with this diagram without any changes?

Update the model if you find anything missing.
There are two main types of validation activities you should do. 

•	that you did the right thing with each threat you found

•	if you found all the threats you should find

If you have a process in place for ensuring that you develop a threat model, document it, and you can increase confidence in your software.

### What does it mean to me :

Treat model start with a simple diagram with all the components included and then introduce trust boundaries to the diagram. Then analyze the system using STRIDE concepts and list down all the possible treats. Then we need to address each and every treat we listed. There are different ways to address threats (Mitigate threats, eliminate threats, transfer threats and accept threats). In verification process need to consider whether we found all the treats and we addressed the all found treats.

### Incident Analyses
### [Analysis of security incident](Analysis%20of%20the%20Security%20incident.md) moved to a seperate link since this is too long to include in this file.

### Starting a lab
### [Starting a lab steps and screen shots](Starting%20a%20lab.md) moved to a seperate link since this is too long to include in this file.
