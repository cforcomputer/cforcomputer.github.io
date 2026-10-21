---
layout: post
title: internet reseller
slug: internet-reseller
---

skills used:
- Wireless networking
- Network zone management
- Enterprise hardware management
- Driver troubleshooting
- Advertising
- Nederlands taal spreken

### Splitting gigabit fiber

One of the things that I put off for way too long at my apartment in Groningen was getting faster internet. The main reason I didn't was simply because I wanted to save money while spending less time in my apartment. Because sitting alone in one's apartment browsing the internet is kind of depressing.

ANYWAY. Finally I was fed up with using the shared apartment wifi. One single 100mbps connection shared between 20 people is not ideal. Oftentimes it wouldn't work at all, and I would write my book instead.

It clicked at some point that since my apartment complex was rent controlled, and attracted the kind of people who also wanted to save money, I could simply offer to split the bill between everyone on the fastest gigabit fiber available, which in this case was 4 Gbps symmetrical fiber since I was in the middle of the city.

I spent several months going back and forth between the store and the Dutch telecom company KPN, and they eventually did send someone out to lay a new line directly to my apartment. Then I wrote on my window advertising the internet share. Two of my neighbors signed up, and I used this as the excuse I needed to spend over a thousand dollars on ubiquiti enterprise networking gear I wanted. 

![Picture of networking setup](assets/images/projects/networking/networking-setup.webp)

The core of the setup was a UniFi Cloud Gateway Fiber running UniFi OS, which handled routing, firewalling, and DHCP for the building. Each household got its own network on a separate VLAN, with a dedicated SSID mapped to it. Using UniFi's zone-based firewall, I placed the tenant networks in their own zone with a default-deny policy between them: every network had internet access, but none could reach the others, and management access to the gateway was restricted to my own network. That kept everyone's smart TVs, speakers, and other IoT devices on their own segment instead of exposed to the whole building.

Wireless ran on a U7 Pro Max (tri-band Wi-Fi 7, including 6 GHz), and everything was uplinked through a compact 10G switch. Exceptionally overkill, but that's what I needed after decades of slow, barely functional internet. The main bottleneck ended up being my own computer: its onboard NIC couldn't keep up with the line rate, so I added a multi-gig network adapter and worked through its driver issues to actually see 4 Gbps.

Cost per person? $20 per month. Everyone including me was very happy. I found that delivering a service that brought relief to people was well worth the money. I think more people could benefit from having side hustle hobbies like this that help their communities. Just do it!