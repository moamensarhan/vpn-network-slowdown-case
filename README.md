Case Study: Network Slowdown Caused by VPN Routing


Overview


Browsing performance degraded suddenly despite stable Wi-Fi baseline conditions. Investigation identified an active VPN connection routing traffic through a geographically distant server, introducing increased latency and degrading web performance.


Environment


OS: Windows 10

Connection: Wi-Fi (consistently weak but normally stable)

VPN Client: ProtonVPN (free tier)

Context: Personal desktop workstation


Reported Symptoms

Significantly slow browsing

Some pages failing to load

Wi-Fi connected and functioning


Initial Assessment


Confirmed Wi-Fi signal strength was consistent with previous normal operation

Tested multiple browsers to rule out application-specific issue

Determined issue was system-wide


Investigation


Opened Resource Monitor → Network tab to inspect process-level network activity.

Observed sustained ~13 Mbps upload and download traffic from ProtonVPN.

This level of continuous throughput was inconsistent with normal browsing behavior.

VPN had auto-connected to a geographically distant server under free-tier restrictions.


Root Cause


An active VPN connection to a distant server introduced additional routing overhead and increased latency, resulting in degraded browsing performance.


Resolution


Disabled ProtonVPN.

Direct ISP routing was restored.


Verification


Browsing speed returned to expected baseline

Pages loaded normally

No further connectivity issues observed
