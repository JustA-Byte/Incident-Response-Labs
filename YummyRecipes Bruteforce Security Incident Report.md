## Preface
After a bruteforce attack was attempted on a web host trying to access an admin account, a company that sells cookbooks has experienced a breach. A javascript function was embeded in the websites source code which prompted visitors to download malware which redirected them to a fake website that provided copies of the cookbooks for free.


## Initial Response
To address the incident, I created a sandbox environment to observe the suspicious website behavior. I ran the network protocol analyzer tcpdump and typed in the URL for the website, yummyrecipesforme.com. As soon as the website loaded, I was prompted to download an executable file to update my browser. I accepted the download and allowed the file to run. I then observed that my browser redirected me to a different URL, greatrecipesforme.com, which was designed to look like the original site. However, the recipes my company sells were now posted for free on the new website.

The HTTP and DNS traffic log displays the following:

![image](https://github.com/JustA-Byte/Incident-Response-Labs/assets/161458321/384ca920-11ba-4f48-943c-f8ba25714d46)


## Incident Report

### Section 1 - Protocols involved in the incident
From the DNS and HTTP traffic log, the 2 network protocols being used are DNS (port 53) and HTTP (port 80). Both protocols are application layer protocols in the TCP/IP stack.

### Section 2 - Incident review
An incident has occurred where customers accessing yummyrecipesforme.com are being prompted to download and run a file which causes there systems to run slowly and redirect them to a new website - greatrecipesforme.com, which seems to be cloning the legitimate website and exposing the businesses intellectual property of recipes for free to the public. 

Contact to the security team was made by the owner of yummyrecipesforme.com saying that they also cannot log into the admin panel for the website either. 

Upon examination of the website source code, Senior Analysts have confirmed that the website has been breached via a brute force password attack, inserting malicious code into the source code which prompts customers to download and run malware which redirects them to the illegitimate website and causes performance issues on their own systems.

Having recreated the issue in a sandbox, I have ran tcpdump and attempted to visit yummyrecipesforme.com, downloaded the file when prompted and was redirected to greatrecipesforme.com where the recipes were readily available for public consumption.

Reviewing the DNS & HTTP traffic log the logs confirm the series of events:
1. At 14:18:32.192571 the client contacts the DNS server using port 53 to find yummyrecipesforme.com and is given the correct IP address
2. Browser is then directed to the correct website using the provided IP address using HTTP over port 80 at 14:18:36.786501
3. Then at 14:18:36.786589 the log indicates a push of data using the [P] flag, and uses a GET HTTP request from my machine to yummyrecipesforme.com. This could be the initial request in the malicious source code that requests the user to download the malware file.
4. Logs then show at 14:20:32.192571 my machine accessing the DNS server over port 53 for the IP address of greatrecipesforme.com and receiving the IP address.
5. My machine then sends the HTTP request to access greatrecipesforme.com at 14:25:29.576493
6. The second to last log at 14:25:29.576590 is another push request from my machine using another HTTP GET command. This could be another request for further malware to be downloaded to the system.

### Section 3 - Recommendations
The priority for remediation is to implement a password policy which includes changing default passwords, creating complex passwords/passphrases on all devices, and also restricting the number of attempts for incorrect passwords. This will significantly reduce the success of any brute force attacks.

Secondary to implementing the password policy, implementing 2FA would ensure additional security, applying the Defence in Depth principle.
