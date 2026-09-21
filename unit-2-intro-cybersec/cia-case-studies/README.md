# Scenario A
1. CIA violation
   - Availability.
2. Secondary impacts
   - Integrity was affected. Patient data has been altered in such a way that only the hackers have access to it.
   The hackers have compromised the integrity of the files and, if they do not receive the ransom, they will be able
   to destroy the files or publish them, for example. Hackers can also alter entries in a patient’s electronic health
   record. They may have their own motives for doing so, but they are still able to edit the files. Furthermore, using
   the documents they have gathered, hackers can forge documents.
   - Confidentiality was also affected, because an unauthorised party gained access to the information and then they
   may publish all data about patients breaching confidentiality. But in reality, they had already breached confidentiality
   the moment they gained access to the files.
3. Attack technique
   - Phishing, using stolen credentials, then privilege escalation (after initially gaining access, they were granted     more extensive privileges.), deleting backups, ransomware.
4. Preventive controls
   - Hospatls' employees could use MFA. Even if hackers got an employee’s password, a single password would
   not be enough to gain access. Also they should filter their emails to avoid falling for phishing emails and train staff to    recognise phishing emails or simply scams.
5. Damage-limitation
   1. Employees should disconnect infected computers from the network to prevent the virus from spreading to other    machines.
   2. Restore data from backups of files that were not attacked yet.
   3. Recruit cybersecurity specialists.
# Scenario B
1. CIA violation
   - Confidentiality
2. Secondary impacts
   - Integrity and availability were not affected, as the hackers did not compromise the integrity of the shop’s data, and the shop remains accessible to everyone.
3. Attack technique
   - Phishing, using stolen credentials, SQL injection, credential dumping.
4. Preventive controls
   - They could use a better password hashing algoritm, than MD5, because MD5 is not secure for storing passwords      and should not be used. Instead, better to use Argon2id, bcrypt or scrypt. MFA and strict access control.         Also it is worth to do a protection against SQL injection to ensure that user input does not become part of       the SQL code.
5. Damage limitation
   1. Immediately close the identified access point and revoke the compromised credentials to prevent further        data leaks.
   2. Reset passwords and switch to a different password storage algorithm.
# Scenario C
1. CIA violation
   - Integrity.
2. Secondary impacts
   - Availability was also affected, because the website was inaccesible for 4 hours, so users could not be          available to the website while it was being restoring from backups.
3. Attack technique
   - Defacement via web vulnerability. The attacker gained the ability to modify the website's content and replaced the home page with a political statement.
4. Preventive controls
   - Website owners can restrict access to the admin panel based on IP address or VPN and enable multi-factor authentication. Update the CMS and web plugins. Apply WAF and continuously monitoring of any changes to the website.
5. Damage limitation
   1. Disable public access to this web service immediately.
   2. If possible, preserve evidence of the attack so that, for example, defenders determine the scale of the        attack.
   3. Restore a website using backups.
# Scenario D
1. CIA violation
   - Integrity.
2. Secondary impacts
   - Confidentiality was compromised because the hacker most likely already knew the info about bank account details. In this way, was compromised the transparency of the information.
3. Attack technique
   - Business email compromise, Social Engineering, Unauthorized data modifictaion. The hackers managed to perfectly mimic the supplier’s email. The victim was taken in by the fake email and opened the file containing account number, which had been edited.
4. Preventive comtrols
   - Apply a DMARC policy to enable the filtering of phishing emails and spam. Enable multi-factor authentication for all staff email accounts. Apply the settings for flagging external emails so that staff can see a label on the email indicating that it is an external email from the internet.
5. Damage limitation
   1. If it possible, request a chargeback through this bank and freeze the account on the reasons of fraud.
   2. Report a crime to Cyber Security Centre.
