## Preface
Upon receiving an unattended USB stick found in a parking lot, I proceeded to examine its contents with caution, utilizing virtualization software to ensure a secure environment. This approach effectively isolated the USB, preventing any potential malware from compromising my system. The investigation revealed the device belonged to a human resource manager, containing a mix of personal and sensitive work-related files.

## Report
### Contents of the USB
The contents of the USB drive seem to be a mixture of both personal and work related files; examples of which are:
- New hire letter
- Vacation ideas
- Employee budget
- Wedding list

Both work and personal files may contain PII, not only of the suggested owner but of other people too. It is not recommended to personal files with work files as any instance of security incidents could expand the surface of affected people and data.

### Attacker Mindset
Information that could be used against Jorge could be done in a malicious way through social engineering attacks against not only Jorge himself but any potential contacts, friends and relatives the files may outline, as well as using potential confidential work related information as attack vectors against the business and it’s employees. 

### Analysis
The USB could be housing malicious programmes within any of the files contained, if this was a baiting exercise. If an employee of the company had obtained the drive, plugged it into their computer and browsed the files, this could trigger any potential malware and infect the host. This could possibly create exposure for the business which may lead to further malware download, could lead to ransomware and data exfiltration should a threat actor want to perform such actions.

If this wasn’t a baiting exercise and Jorge accidentally dropped the drive in the car park, the PII contained could be used by threat actors against him or anybody else outlined within the drive itself. This may lead to identity theft, social engineering attacks, attacks on the business and more.

Recommended actions to combat negative outcomes noted above are:
- Implement port security on local hosts, to limit the use of USB drives
- Provide employee awareness training of these kinds of events and the effects it can have on businesses and people in general
- Implement EDR, AV and firewall solutions on hosts to warn of potential malicious events happening within the business

