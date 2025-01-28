# Phishing Email Investigation: Identifying and Analyzing a Threat

**Introduction:** _This project focuses on investigating a phishing email received by my dad, showcasing my ability to analyze and respond to real-world cybersecurity threats. The analysis includes examining email headers, investigating suspicious links and attachments, and leveraging tools like VirusTotal and OSINT methods to trace the attack's origin._

Throughout this project, I'll gain hands-on experience with the following concepts and skills:

* Email Header Analysis: Extracted and analyzed email metadata to trace the sender's IP and domain.
* Threat Intelligence Tools: Used MXTool and Kali Linux platforms to investigate suspicious links and attachments.
* Incident Documentation: Created detailed reports on phishing tactics and recommendations for prevention.
* Secure Analysis Practices: Conducted all investigations in a controlled environment to prevent system compromise.

**Tools:** To complete this project, I will use the following tools:\

**Email Header Analyzer:** To analyze email headers and trace the sender.
**WHOIS:** To gather domain registration information for the sender's email or IP address.
**IP Geolocation Services:** To identify the physical location of the sender’s IP.
**VirusTotal: ** To analyze any links or attachments in the email for potential threats.
**Malware Analysis Tools:** If you have the malware file, tools like Cuckoo Sandbox or Hybrid Analysis can help you safely analyze the content.

# Step 1: Gather and Preserve Evidence
I've started by saving the email as an .eml or .msg file to preserve the metadata and headers for my analysis. Below are the listed contents of the email:

* **Sender's email address:** cineastesebt@gmail.com
* **Time message sent:** January 26, 2025 at 10:08:02
* **Subject line and body text:** (Our home address) Dr Vilsaint, this will remain confidential 
* **Any attachments or links:** A .txt file

# Step 2: Analyzing Email Headers
After gathering and preserving the evidence, I was able to paste the header into **MX ToolBox** and resulted with the email following a series of hops through multiple servers with varying time delays. Initially, it passed through the server hermes--production-bf1-66bb576cbb-p5m6b, with no significant delay. The second hop took 3 seconds as the email was routed through sonic.gate.mail.ne1.yahoo.com and sonic304.consmr.mail.bf2.yahoo.com. The third hop, which occurred in just 1 second, involved the server sonic304-11.consmr.mail.bf2.yahoo.com (IP: 74.6.128.34), a known blacklisted IP, indicating that the email may be suspicious or potentially malicious. Finally, the email was routed through an IPv6 address (2002:a05:6214:2f90:b0:6d4:249e:92fd) using SMTP with no notable issues. The analysis of the hops confirms that the email originated from a suspicious server that is flagged for involvement in spam or malicious activity, adding to the evidence that the email may be part of a phishing attempt.

* Senders IP Address: Received: from sonic304-11.consmr.mail.bf2.yahoo.com (sonic304-11.consmr.mail.bf2.yahoo.com. [74.6.128.34])
* Domain aka Return-Path: (Fathers email address)

# Step 3: IP Location of Sender
I performed a WHOIS lookup on the suspicious IP address (74.6.128.34), which revealed that it belongs to Oath Holdings Inc., a subsidiary of Verizon and the parent company of Yahoo. The IP falls within the range 74.6.0.0 - 74.6.255.255 and is part of the INKTOMI-BLK-6 network. The organization’s abuse contact, network-abuse@cc.yahoo-inc.com, is listed, indicating potential monitoring for malicious activities. This information helped identify the IP's ownership and provided a point of contact for reporting the phishing incident.

The WHOIS query on the IP address (74.6.128.34) revealed the following information:

IP Range: 74.6.0.0 - 74.6.255.255
Network Name: INKTOMI-BLK-6
Organization: Oath Holdings Inc. (formerly part of Yahoo)
Address: 770 Broadway, New York, NY 10003-9558, United States
Registration Date: February 13, 2006
Updated Date: March 22, 2019

# Step 4: Analyzing Phishing Indicators
The phishing email uses threatening tactics to manipulate the recipient into paying a ransom. The sender threatens to release embarrassing video footage to the victim’s contacts unless a payment is made. The sender offers a "pay to keep it secret" option, demanding $2000 in Bitcoin. This creates a sense of urgency and fear to coerce the recipient into paying. The payment is only accepted in Bitcoin, a common method used to evade traceability, adding to the scam’s malicious intent.

# Step 5: Scam Analysis
The scam email uses fear, manipulation, and false promises to prey on the victim’s emotions and personal vulnerabilities. It capitalizes on shame and embarrassment and manipulates the victim into paying a ransom to protect their reputation. By leveraging personal details and creating a sense of urgency, the scammer aims to pressure the victim into making an impulsive decision, without considering the legitimacy of the situation. This is a classic example of how personal information can be exploited in phishing attacks to deceive and defraud victims.

# Step 6: Prevention Recommendations
To help my dad avoid falling for phishing attacks, I explained the importance of being cautious when viewing emails. Key practices include checking the sender's email address for legitimacy, being aware of common signs like spelling errors or suspicious language, and being cautious of ransom demands or threats. I also recommended downloading Netgear Armor, which allowed us to run a scan on his device to detect any suspicious activity. Additionally, I set up a VPN for him to ensure his browsing is more secure and enabled browsing protection to further safeguard against potential threats. These steps will help protect against future phishing attempts and enhance his overall security online. The email was reported as a phishing attempt and sent to the Oath Holdings Inc. to make them aware of the senders email and IP address.

**Screenshots are uploaded**

# Below is an edited copy of the email suppressing confidential information.


First Alternative is to turn a blind eye to this email message. Let me tell you what is going to happen if you take this path. I will send your video to all of your contacts. The video was straight fire, and I can't even fathom the embarrasement you'll face when your colleagues, friends, and fam see it. But hey, that's life, ain't it? Don't be playing the victim here. 

Other option is to pay me, and be confidential about it. We’ll name it my “keep the secret charges”. Lets discuss what will happen if you go with this way out. Your secret will remain private. I will destroy all the data and evidence once you come through with the payment. You need to make the payment through Bitcoins only. I want you to know I'm aiming for a win-win here. I will keep my end of the bargain.



Amount to be sent: $2000

BTC ADDRESS: bc1qd874nsl58ruh5ww7c5ktp4mkv2z55fuzl34mv8



Once you pay up, you'll sleep like a baby. I keep my word.



And of course: You got one day to sort this out and I will only accept Bitcoin. I have a unique pixel in this e-mail, and now I've been notified that you have read this message. This email and Bitcoin address are custom-made for you, untraceable. If you are unfamiliar with Bitcoin, google it. You can buy it online or through a Bitcoin ATM in your neighborhood.	There's no point in replying to this email or negotiating, it's pointless my price is fixed. As soon as you send the complete payment, my system will inform me and I will wipe out all the dirt I got on you. Remember if I catch that you've shared or discussed this message with anyone else, your shitty video will instantly start getting sent to your contacts and I will post a physical tape to all of your neighborhood next week. And don't even think about turning off your phone or resetting it to factory settings, I already have all your data. I don't make mistakes, Farine.

Honestly, those online tips about covering your camera aren't as useless as they seem. Now, I am waiting for my payment..



