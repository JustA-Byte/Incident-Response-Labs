## Preface
YummyRecipes' customers have reported that when attempting to visit the website they are presented with the error "destination port unreachable". Having received the same message myself, I boot up tcpdump and load the webpage again. The DNS & ICMP traggic log is shown below:

![image](https://github.com/JustA-Byte/Incident-Response-Labs/assets/161458321/c7e3b795-408e-42ee-a089-c226197e231d)

## Summary
The network protocol analyser logs outline that there is a problem with UDP port 53 being unreachable. Port 53 being assigned to DNS would indicate there is an issue with the DNS server not being available. This could stipulate that there may be a security issue or ongoing malicious attack on the DNS server.

## Analysis and Explanation
The incident began early this afternoon when users were trying to access the website yummmyrecipesforme.com and after waiting for some time, users were presented with the message ‘destination port unreachable’. 

Having received reports of this, the Network Security team attempted to access the website and were faced with the same message. We then utilised the tcpdump network protocol analyser to capture packets when trying to access the website. The analyser logs, taken at 13:24:32-13:28:50, indicate that the ICMP response shows UDP port 53 is unreachable. This would indicate no service was listening on the receiving DNS port as indicated by the ICMP error message “udp port 53 unreachable.”

The next steps are to check the firewall to ensure port 53 isn’t being blocked, potentially flush the DNS cache from devices to see if that allows new DNS resolution. It is reasonable to check if the DNS service is down due to a DoS attack.
