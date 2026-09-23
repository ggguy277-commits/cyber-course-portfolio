# 1. The incident
The WannaCry attack was on 12 May in the morning 2017.

WannaCry exploited a vulnerability in Windows’ SMB protocol. Although Microsoft had patched this vulnerability 
in its latest update, most devices had not been updated and were therefore got attacked by this virus. This virus 
was a worm, so once it had infected one computer, it looked for ways to spread to other devices. 
When WannaCry infected a device, it encrypted all the data and demanded a ransom of 300 bucks in Bitcoin and, over time, 
if the victim failed to pay the ransom on time, the ransom would double (600 dollars in Bitcoin). This virus spread so 
rapidly that by the evening of 12 May it had infected 200k devices worldwide. The virus has affected around 603 healthcare 
organisations in Britain. It has disrupted thousands of operations and appointments. The virus has also affected Nissan in UK,
Renault, transport in Germany, telecommunications etc.
# 2. Who was affected
National Health Service (NHS) in UK, auto industry, german trains Deutsche Bahn, telecommunication companies such as Telefonica, Megafon,
FedEx, factories etc. Yes timing played an important role because practically everyone didn't update their software.
# 3. CIA
Availability and Integrity were affected. Availability, because virus made all data on computers inaccessible and integrity, 
because data was edited to make it inaccessible. Confidentiality was not affected, attackers did not leaked the data.
# 4. The attack technique 
WannaCry was ransomeware and worm at the same time.

Ransomeware is a programme that encrypts a user’s data, making it inaccessible until the victim transfers cryptocurrency to the virus 
creator’s wallet. The worm-like capabilities of this virus made it more dangerous than typical ransomware viruses, because the programme 
did not require the involvement of both parties to spread, it found its own way to other devices.
# 5. How it was discovered and how it was stopped
A researcher Marcus Hutchins discovered accidently a vulnerability in the virus – sort of like an emergency stop button (kill switch). The sense of it was 
that the virus asks, ‘Can I connect to a specific domain name?’, which looked like a random string of letters ending in .com. When the programme connects to the domain, it stops working. Then he discovered this, he registered the domain for 10 bucks. Now the virus can connect to that domain, and as a result, it stops working.
# 6. What could have helped
The thing is that automatic system updates were disabled on most computers. It would probably be a good idea to phase out systems running Windows XP and Windows Server 2003, since Microsoft no longer supports them. It's also a good idea to have backup of files in case a virus has already infected device.
# 7. The broader lesson
A major international cyber incident may arise not because of some super technology, but due to a combination of a known vulnerability, a missing update, outdated infrastructure and a leaked government tool.
# 8. Personal takeaway
I suppose this incident has changed my view on software updates and just how important they can be.
