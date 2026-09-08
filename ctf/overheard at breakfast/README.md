## TryHackMe Overheard at Breakfast CTF Writeup
Two strangers. One conversation. One profile they never meant to reveal.

**Category:** OSINT, Social Media, Hashing.

**CTF Date:** August 1, 2026.

<img src="https://github.com/Daneyal-Bajwa/Writeups/blob/main/ctf/overheard%20at%20breakfast/images/brief.png" alt="A brief describing the hotel breakfast setting" width="600" align="center">

###### Figure 1 – Background story provided by the challenge

## TL;DR

We reveal a _hidden account_ using a _screenshot_ of a conversation and **Gravator**, an online platform linking all your online profiles to a single digital identity.
## Overview:
We begin with a brief description of a hotel breakfast, and someone snooping a private text conversation. When the recipient of the snooping steps away, the person quickly takes a picture of the text conversation on their device. **Our objective is to use the information provided in the picture to find their hidden account.**

<img src="https://github.com/Daneyal-Bajwa/Writeups/blob/main/ctf/overheard%20at%20breakfast/images/conversation.png" alt="Conversation between target and their acquaintance" width="800" align="center">

###### Figure 2 – The private conversation picture, provided as a downloadable file in the challenge

During initial inspection, we are provided with the following information: the target’s name is Lambo, they are speaking to an influencer named Ponzi, and Lambo is staying at a hotel called Byte Lotus.

As we read on, we are also provided the following: 

* an account linking service beginning with the letter **G**

* the _email address_

The service points to **Gravatar**, where all your online accounts are linked to a single digital identity linked to your email.
Visiting Gravator, the following web page is shown:

<img src="https://github.com/Daneyal-Bajwa/Writeups/blob/main/ctf/overheard%20at%20breakfast/images/gravator.png" alt="Gravator landing page showing a text box where you can type in an email address to search for someone" width="600" align="center">

###### Figure 3 – Gravator landing page 
 
We can type in the _email address_ into the **text box**, which shows us this:

<img src="https://github.com/Daneyal-Bajwa/Writeups/blob/main/ctf/overheard%20at%20breakfast/images/profile.png" alt="Profile of the target with the description including some hash" width="400" align="center">

###### Figure 4 - Target's profile on Gravator
 
The _‘prize’_ of the profile uses _uppercase, lowercase and numbers_. This points to a **base-64 hash**. Decoding it in your terminal results in the flag!

<img src="https://github.com/Daneyal-Bajwa/Writeups/blob/main/ctf/overheard%20at%20breakfast/images/terminal.png" alt="Terminal decoding the hash to reveal the flag" width="600" align="center">

###### Figure 5 - The hash decoded in the terminal to reveal the flag



