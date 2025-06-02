# CYBER SECURITY INTERNSHIP - TASK 5  
**Network Traffic Analysis with Wireshark**  
*Capturing and Identifying Protocols*  

---

## 📝 Task Overview  
**Objective**: Capture live network packets using Wireshark and identify protocols (DNS, HTTP, ICMP, TCP/UDP).  

**Tools Used**:  
- Wireshark (Kali Linux pre-installed)  
- Terminal commands (`ping`, `nslookup`, `curl`)  

---

## 🛠️ Steps Executed  

### 1. **Capture Setup**  
- Selected interface `eth0` in Wireshark.  
- Generated traffic for 2 minutes:  
  ```bash
  ping google.com -c 5                # ICMP packets
  curl http://example.com            # HTTP traffic
  nslookup google.com                # DNS query
  ```
## 2. Protocol Identification
Applied Wireshark filters:

| Protocol | Filter | Example Packet |
|----------|--------|----------------|
| **DNS**  | `dns`  | `Standard query google.com` → Response `A 142.250.190.46` |
| **HTTP** | `http` | `GET / HTTP/1.1` to `example.com` |
| **ICMP** | `icmp` | `Echo (ping) request` to `8.8.8.8` |
| **TCP**  | `tcp`  | `[SYN]`, `[ACK]` handshake packets |
