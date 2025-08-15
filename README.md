# VPN Analysis – ProtonVPN (Free Tier)

## Objective
Understand the role of VPNs in protecting privacy and enabling secure communication by analyzing ProtonVPN's functionality and protocol usage in its free tier.

## Overview
A **Virtual Private Network (VPN)** creates an encrypted tunnel between your device and a VPN server, hiding your IP address and securing your data from interception. This helps protect privacy, prevent ISP tracking, and safeguard connections on insecure networks like public Wi-Fi.

## Tools & Setup
- **VPN Service**: ProtonVPN (Free Tier)
- **Analysis Tool**: Wireshark (for packet capture)
- **OS**: Linux

## Observations
- **Protocol Used**: WireGuard (UDP)
- **Encryption**: ChaCha20 (for data encryption) and Poly1305 (for authentication)
- **Traffic Behavior**:  
  - All internet traffic routed through a single VPN server IP.
  - Packet payloads appear as random binary data (encrypted).
  - No visible DNS or HTTP requests in plaintext — DNS queries are also tunneled.
- **Server Location**: Based on free-tier server availability, typically US, Netherlands, or Japan.

## Benefits of Using VPN
- Encrypts data to protect from eavesdropping.
- Masks your IP address to enhance anonymity.
- Secures communication over public and untrusted networks.
- Helps bypass some geo-restrictions.

## Limitations
- Slight reduction in internet speed due to encryption overhead.
- Free tier offers limited server locations and sometimes lower speed.
- Cannot protect against threats outside the tunnel (e.g., phishing, malware).

## Conclusion
ProtonVPN’s free tier uses **WireGuard** with strong encryption (ChaCha20-Poly1305) to ensure secure, private communication. It effectively hides IP addresses and encrypts all traffic, fulfilling the core privacy and security objectives of a VPN.

