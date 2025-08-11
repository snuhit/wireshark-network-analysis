# Network Traffic Analysis Report

**Date:** 11 Aug 2025  
**Tool Used:** Wireshark  
**Capture Duration:** ~1 minute  
**Target Site:** http://example.com  

---

## Protocols Identified

### 1. DNS
- **Purpose:** Resolves `example.com` domain to an IP address.
- **Transport Protocol:** UDP (port 53).
- **Observation:**  
  - A DNS query packet was sent from my machine to the DNS server requesting the A record for `example.com`.  
  - The DNS server responded with the IP address `93.184.216.34`.

### 2. TCP
- **Purpose:** Establishes a reliable connection between client and server.
- **Observation:**  
  - The TCP three-way handshake (SYN → SYN-ACK → ACK) occurred between my machine and the `example.com` server.
  - TCP segments carried HTTP request and response data.

### 3. HTTP
- **Purpose:** Transfers unencrypted web content between client and server.
- **Observation:**  
  - Sent an HTTP GET request for `/` to `example.com`.  
  - The server responded with HTTP 200 OK along with HTML content of the landing page.  
  - Headers and content were fully visible because the site uses HTTP (port 80) instead of HTTPS.

---

## Key Observations
- DNS queries were visible and easy to filter with `dns` in Wireshark.
- TCP handshake packets confirmed a successful connection establishment before HTTP data transfer.
- HTTP traffic was in plaintext, allowing inspection of request headers, server response headers, and the HTML body.

---

## File
- **Packet Capture:** `Network_capture.pcap`  
