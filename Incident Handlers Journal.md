# Incident handlers Journal

| **Date** <br> 12/08/2023 | **Entry:** <br> 1.0                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------|
|        Description       | A breakdown of a scenario surrounding a US based health care clinic that has suffered a ransomware attack. |
|       Tool(s) Used       | None                                                                                                       |
|       The 5 W's          | **Who caused the incident?** <br>- The incident was caused by a well known organised group of unethical hackers known for targeting healthcare institutes. <br>**What happened?** <br>- Employees were targeted with phishing emails that contained attachments laced with malware. This malware once activated downloaded ransomware files, encrypted the local machine files, including critical patient data, and left a ransomware note on the screen of the local computers. <br> **When did the incident occur?** <br>- Approximately 9am on Tuesday morning. <br> **Where did the incident happen?** <br>- A small US based healthcare clinic specialising in delivering primary-care services. <br> **Why did the incident happen?**<br>- Employees who were targeted unknowingly opened the phishing email attachments which triggered the malware download. The hacking group want to extort the business for money to release access to patient files and data. |
| Additional Notes | The company was forced to shut down their computer systems and contact several organisations to report the incident and receive technical assistance. This means that not only have they suffered a financial cost to this event, there is a reputational damage to consider, damage to customer privacy due to their data being accessed and also general patient care, where patients haven’t been able to be dealt with, they have been left to suffer unnecessarily. |


<br><br>


| **Date** <br> 16/08/2023 | **Entry:** <br> 2.0                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------|
|        Description       | Investigating and analysing a suspicious file hash. |
|       Tool(s) Used       | Pyramid of pain, SHA-256, VirusTotal                                                                      |
|       The 5 W's          | **Who caused the incident?** <br>- Malicious actors wishing to infect host systems within the business. <br>**What happened?** <br>- A phishing email was sent to an employee which had a password protected attachment containing malware. Once the file was accessed using the password, the malware activated and further executable files were created on the host system. <br> **When did the incident occur?** <br>- between 1:11pm-1:20pm. <br> **Where did the incident happen?** <br>- an employee’s computer at a financial services company. <br> **Why did the incident happen?**<br>- malicious actors wanting access to the system to steal input information. |
| Additional Notes | This seems like the initial stages of infection that could lead to more severe outcomes like customer data exfiltration. The malware included data input monitoring, defensive evasion techniques and direction to malicious URLs. Poorly configured IDS may not have picked this malware up which could definitely have caused harm to customer and company data. VirusTotal showed multiple reports of the file being malicious in intent with sandboxed reports showing information around network connections, relations, behaviour of the malware and TTPs. |


<br><br>


| **Date** <br> 18/08/2023 | **Entry:** <br> 3.0                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------|
|        Description       | Responding to a malicious phishing alert using an incident response playbook |
|       Tool(s) Used       | Playbook, VirusTotal, Security alert                                                                     |
|       The 5 W's          | **Who caused the incident?** <br>- External threat actors attempting to compromise business systems. <br>**What happened?** <br>- An email was sent to the business containing a potentially malicious attachment which may have been opened by the employee it was sent to. The security system has flagged the email and sent an alert to the security team for review. <br> **When did the incident occur?** <br>- Wednesday, July 20th 2022, 09:30:14 <br> **Where did the incident happen?** <br>- Financial services company on an employee computer <br> **Why did the incident happen?**<br>- Threat actors attempting to infect company systems, the employee not realising the email was malicious and opening the attachment. |
| Additional Notes | VirusTotal shows the attachment file hash as being malicious. The email itself has multiple areas that indicate a phishing attempt: <br>- The email address of the sender doesn’t match the name of the sender and is suspicious. <br>- The subject line begins as a reply. <br>- There is a typo in the greeting. <br>- Bad grammar in the body of the message. <br>- The body specifies that there is a resume and cover letter attached, however the attachment is a single executable file. <br>- I have updated the alert document as required by the playbook and marked the case for escalation due to being malicious. |
