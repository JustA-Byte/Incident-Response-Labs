# Incident report analysis

## Summary
The company experienced network issues, network services suddenly stopped responding and normal internal network traffic could not access any network resources. Incident management found that the issues were due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources for 2 hours during the ongoing attack until resolved.

## Identify
The Incident Management team initially reacted to the situation which led to the Cybersecurity Team investigation which found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack. 

## Protect
The security team implemented a new firewall rule to limit the rate of incoming ICMP packets and source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets. By doing so the firewall will actively filter ICMP traffic incoming into the business reducing the probability of this attack being as effective in the future, reducing risk to the businesses internal network.

## Detect
To detect abnormal traffic patterns and filter out some ICMP traffic based on suspicious characteristics the security team implemented network monitoring software and an IDS/IPS system. This will increase the response time and reduce the risk of experiencing a similar attack in the future.
The implementation of a SIEM tool in the future could also help with the monitoring of these new systems that have been implemented due to the centralisation of network logs and visibility of dashboards.

## Respond
The incident management team responded by blocking incoming ICMP packets and take all non-critical network services offline.

For future incidents utilising the new systems put in place, highlighted under the ‘Detect’ section of this report, the incident management team will be able to respond much quicker to similar attacks due to improved network traffic monitoring. 

Communications between teams should be done through dedicated encrypted channels via key stakeholders for situational updates. Possible strategies to avoid whole internal network failure in the future could be the implementation of network segmentation or the use of a DMZ separating the internal network from the internet by another firewall. In doing this potentially only certain sections of the internal network would be affected and not the whole network, causing a smaller disruption to the business overall.

## Recover
From the initial response  of the incident management team, they were able to restore critical network services, allowing IT teams to bring systems back online in order of priority and return to normal working order. 

Communications should be sent to the wider employee base with brief descriptions of what has happened and explaining system functionality has returned.

Lessons learned from the situation should be recorded in the company’s incident response playbook so that incident responders can be more responsive and effective if another attack of this nature should occur.
