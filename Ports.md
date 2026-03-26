- Ports are logical endpoints on a computer used by services.
- IP = identifies the machine
- Port = identifies the service on that machine

E.g., 192.168.1.10:80  = web server

### Port Ranges

- 0-1023 --> well known ports
- 1024-49151 --> Registered
- 49152-65535  --> Dynamic/private

### Well Known Ports + Attacks

| Port    | Service | Risk Level | Common Attacks                                                                                                          | Key Attack            |
| ------- | ------- | ---------- | ----------------------------------------------------------------------------------------------------------------------- | --------------------- |
| 21      | FTP     | High       | - Brute force login   -Anonymous login               - Sniffing credentials ( plain text)                               | Sniffing, brute force |
| 22      | SSH     | Medium     | - Brute force attack               - Credential stuffing             - Key based attacks (if misconfigured)             | Brute force           |
| 23      | Telnet  | High       | -Password sniffing                 - Man in the Middle              -Brute force                                        | MITM, sniffing        |
| 25      | SMTP    | Medium     | -Email spoofing                    -Spam relay (open relay abuse)                                    - phishing attacks | Spoofing              |
| 53      | DNS     | High       | -DNS spoofing / Poisoning    - DNS amplification (DDoS)  - cache poisoning                                              | Poisoning             |
| 80      | HTTP    | High       | -Man in the Middle                - Session hijacking                - XSS (cross site scripting)     -SQL injection    | XSS, MITM             |
| 443     | HTTPS   | Medium     | - SSL/TLS attacks<br>- Certificate spoofing<br>- Downgrade attacks<br>- Still vulnerable to XSS / SQL injection         | TLS attacks           |
| 139/445 | SMB     | Critical   | - EternalBlue exploit (used in WannaCry ransomware attack)<br>- Null session attack<br>- SMB relay attack               | EternalBlue           |
| 3389    | RDP     | Critical   | - Brute force<br>- BlueKeep exploit<br>- Session hijacking                                                              | Brute force           |