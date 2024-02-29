## Introduction
I have used the <a href="https://github.com/JustA-Byte/Incident-Response-Labs/blob/main/Phishing%20Incident%20Response%20Playbook.md">Phishing Incident Response Playbook </a> to address the following Phishing email alert.

| Ticket ID | Alert Message | Severity | Details | Ticket Status|
|-----------|--------------|-----------|---------|--------------|
| A-2703    | SERVER-MAIL Phishing attempt possible download of malware| Medium | The user may have opened a malicious email and opened attachments or clicked links. | Escalated|

<br>

| Ticket Comments |
|-----------------|
| VirusTotal shows the attachment file hash as being malicious. The email itself has multiple areas that indicate a phishing attempt: <br>- The email address of the sender doesn’t match the name of the sender and is suspicious. <br>- The subject line begins as a reply
There is a typo in the greeting. <br>- Bad grammar in the body of the message. <br>- The body specifies that there is a resume and cover letter attached, however the attachment is a single executable file. <br>- Escalating the alert to level 2 SOC analysts for further investigation and action as per the playbook process. |

<br>
### Additional Information
**Known malicious file hash**
54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b <br>

<br>

Email received: <br>
From: Def Communications <76tguyhh6tgftrt7tg.su>  <114.114.114.114> <br>
Sent: Wednesday, July 20, 2022 09:30:14 AM <br>
To: <hr@inergy.com> <176.157.125.93> <br>
Subject: Re: Infrastructure Egnieer role <br>

Dear HR at Ingergy,

I am writing to express my interest in the engineer role posted from the website.

There is attached my resume and cover letter. For privacy, the file is password protected. Use the password paradise10789 to open. 

Thank you,

Clyde West
Attachment: filename="bfsvc.exe"



