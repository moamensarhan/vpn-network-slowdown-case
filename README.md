Case Study: Network Slowdown Caused by VPN Routing

---
Overview

Browsing became significantly slower despite Wi-Fi signal strength remaining consistent with prior normal operation. Investigation revealed an active VPN connection routing traffic through a geographically distant server, increasing latency and affecting page load times.

---

Environment

OS: Windows 10

Connection: Wi-Fi (consistently weak but normally stable)

VPN Client: ProtonVPN (free tier)

Context: Personal desktop workstation

---

Reported Symptoms

Significantly slow browsing

Some pages failing to load

Wi-Fi connected and functioning

---

Initial Assessment

Confirmed Wi-Fi signal strength was consistent with previous normal operation

Tested multiple browsers to rule out application-specific issue

Determined issue was system-wide

---

Investigation

The slowdown was observed across multiple browsers on the desktop. A separate device (mobile phone) on the same Wi-Fi network functioned normally, indicating the issue was isolated to the PC rather than the network itself.

Resource Monitor was opened to inspect process-level network activity.

Resource Monitor showed sustained network activity from ProtonVPN, fluctuating between approximately 10–15 Mbps in both directions. 

Further inspection confirmed the VPN had auto-connected to a geographically distant server under free-tier restrictions.

<img width="1127" height="148" alt="vpn-bandwidth-usage" src="https://github.com/user-attachments/assets/34b749f6-85ce-47d5-a427-79267c19f2bf" />

---

Root Cause

Traffic was being routed through a distant VPN endpoint, increasing latency and negatively impacting web responsiveness.

---

Resolution

ProtonVPN was disabled, as switching to a geographically closer server was unavailable under the free-tier plan.

---

Verification

Browsing performance returned to expected baseline levels, and pages loaded normally without delay.

No further connectivity issues observed
