1. Install Wireshark
- Download the installer from the official [Wireshark website](https://www.wireshark.org/).
- Install following default options (ensure **Npcap** or **WinPcap** is installed for packet capture).

### 2. Start Capturing Traffic
- Launch Wireshark.
- Select the active network interface (e.g., Wi-Fi or Ethernet).
- Click to start capturing packets.

### 3. Generate Network Traffic
- Open a browser and visit any website **OR**
- Run `ping google.com` in the terminal/command prompt.

### 4. Stop the Capture
- Wait ~1 minute.
- Click the red **Stop** button.

### 5. Filter Packets by Protocol
- Use the top filter bar:
  - `dns` — Domain Name System queries
  - `tcp` — Transport connections
  - `http` — HTTP traffic (if unencrypted)

### 6. Identify Different Protocols
Look at the **Protocol** column. Common examples:
- **DNS**
- **TCP**
- **HTTP/HTTPS**
- (ICMP if you pinged a server)

### 7. Export the Capture
- `File` → `Save As` → select `.pcap` format.

### 8. Summarize Findings
Example:

| Protocol | Function | Example Packet |
|----------|----------|----------------|
| DNS      | Resolves domain names | Query for `www.example.com` |
| TCP      | Connection management | SYN/ACK handshake packets |
| HTTP     | Web content requests | GET `/index.html` |
