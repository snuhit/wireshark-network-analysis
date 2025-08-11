# Wireshark Network Traffic Analysis

## Objective
Capture live network packets and identify basic protocols and traffic types.

## Steps Taken
1. Installed Wireshark on Mac M1.
2. Started capture on active network interface (`en0`).
3. Visited HTTP and HTTPS websites to generate traffic.
4. Applied filters for DNS, HTTP, and TCP.
5. Saved the capture as `network_capture.pcap`.
6. Documented findings in `report.md`.

## Contents
- `Network_Capture.pcap` → Raw packet capture file.
- `report.md` → Summary of identified protocols.
- `screenshots/` → (Optional) Wireshark screenshots.

## Tools Used
- Wireshark (free)
- macOS Terminal for ping command

## Key Learnings
- How to capture live packets on an interface.
- Identifying protocols with filters.
- Understanding differences between HTTP, HTTPS, DNS, and TCP.
  
## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
