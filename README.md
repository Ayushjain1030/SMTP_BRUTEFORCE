An SMTP brute force attack is a cyberattack that systematically guesses username and password combinations to gain unauthorized access to a mail server. By targeting the Simple Mail Transfer Protocol (SMTP), attackers aim to hijack email accounts to send spam, phishing emails, or steal sensitive information. 
Proofpoint
Proofpoint
 +4
How SMTP Brute Force Works
Targeting SMTP AUTH: Attackers connect to the SMTP server (usually on port 587 or 465) and attempt to authenticate using valid SMTP credentials.
Automated Guessing: Using automated tools (e.g., Hydra, Nmap), they try thousands of common passwords or dictionaries against specific usernames.
Enumeration: Attackers often use commands like VRFY, EXPN, or RCPT TO to verify valid usernames on the system before starting the password guessing phase.
Password Spraying: A common variation where attackers use a single popular password against many accounts to avoid triggering account lockouts. 
Microsoft Community Hub
Microsoft Community Hub
 +5
The Role of SMTP in Attacks
SMTP servers are high-value targets because they often store sensitive information and provide access to email systems. 
Packt
Packt
Initial Access: Attackers use brute force as an entry point to compromise systems (T1110 in MITRE ATT&CK).
Open Relay Exploitation: If a server is misconfigured as an "open relay," attackers can use it to send massive amounts of spam without needing credentials, ruining the domain's reputation.
Account Takeover: Successful attacks can allow hackers to send phishing emails internally, making them more trustworthy. 
ScienceDirect.com
ScienceDirect.com
 +3
Mitigation and Defense
Implement Strong Password Policies: Enforce complex, unique passwords to make guessing attempts inefficient.
Enable Rate Limiting & Account Lockouts: Detect multiple authentication failures and temporary block IPs or accounts.
Disable Basic Auth: Transition to Modern Authentication (OAuth) and disable legacy Basic Authentication for SMTP client submissions, as recommended for Exchange Online.
Use Firewalls & IP Whitelisting: Use tools like Fail2Ban or firewall rules (e.g., CSF) to block IPs that show malicious behavior.
Configure SPF, DKIM, DMARC: Secure the domain to prevent spoofing and unauthorized relaying. 
Microsoft Learn
Microsoft Learn
 +7
