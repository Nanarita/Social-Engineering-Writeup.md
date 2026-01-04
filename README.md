# Social-Engineering-Writeup.md
Documentation of technical analysis for social engineering exercises. This repository covers email header forensics, phishing indicator identification, and threat intelligence gathering.
Phishing Analysis Fundamentals
Scenario Overview
This lab focuses on the fundamentals of email forensics and phishing analysis. As a security analyst, I analyzed email structures, headers, and bodies to identify malicious intent and gather threat intelligence.

Task 2: Email History & Structure
Question: Email dates back to what time frame?

Answer: 1970s.
<img width="1593" height="203" alt="image" src="https://github.com/user-attachments/assets/46ea6819-fdc9-4909-a26a-55daaefbaf05" />


Key Learning: An email consists of a user mailbox and a domain (e.g., billy@johndoe.com).

Task 3: Email Protocols
I identified the secure ports used for various email retrieval and transmission protocols:

Secure SMTP (STARTTLS): Port 587.

Secure IMAP: Port 993.

Secure POP3: Port 995.
<img width="1594" height="458" alt="image" src="https://github.com/user-attachments/assets/ecef6a1a-b37a-43f6-a218-8497573b0341" />


Task 4: Email Header Analysis
Analyzing headers is critical for tracing the origin and path of an email.

Reply-To Header: This field is functionally the same as the "Return-Path" or specific "Reply-To" address, which can differ from the "From" address to trick users.

Finding Source IP: I examined the X-Originating-IP or the lowest Received header to find the sender's true IP address.

IP Information: After identifying the IP, tools like iplocation.net were used to retrieve geographical data.
<img width="1576" height="320" alt="image" src="https://github.com/user-attachments/assets/f7934ba6-31e6-47f2-be04-291cce1047b9" />


Task 5: Email Body & Attachments
Attachment Analysis: Malicious attachments are often encoded in Base64.

Headers to Check:

Content-Type: application/pdf.

Content-Disposition: Specifies if the file is an attachment.

Content-Transfer-Encoding: Often set to "base64" for binary files.
<img width="1577" height="455" alt="image" src="https://github.com/user-attachments/assets/89b3bcab-e481-4381-b359-fc995f26331b" />


Task 6: Common Phishing Characteristics
Attackers use various techniques to deceive victims:

Masquerading: Spoofing trusted entities (e.g., Amazon, PayPal).

Urgency: Using keywords like "Invoice," "Suspended," or "Urgent".

<img width="1582" height="594" alt="image" src="https://github.com/user-attachments/assets/44c0efcc-ad1a-4366-89cd-f5c3941f1a0d" />

Defanging: For reporting purposes, I practiced defanging URLs (e.g., hxxp[://]malicious[.]com) to prevent accidental clicks.

<img width="1363" height="872" alt="image" src="https://github.com/user-attachments/assets/6c2fcae8-6f85-4f11-b7a0-3a48d373530f" />
