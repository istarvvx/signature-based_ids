# Intrusion Detection System (IDS)

A lightweight and effective Intrusion Detection System designed to monitor network traffic for suspicious activity and known threats. This project helps secure networks by analyzing packets in real-time and alerting administrators to potential security breaches.

## Features
*   **Real-time Packet Sniffing:** Continuously captures and analyzes incoming and outgoing network traffic.
*   **Rule-Based Detection:** Compares network activity against a customizable set of known malicious signatures.
*   **Anomaly Detection:** (Optional) Flags unusual traffic patterns that deviate from standard network behavior.
*   **Automated Alerting:** Generates immediate warnings (via console, log files, or email) when suspicious activity is detected.
*   **Detailed Logging:** Maintains comprehensive records of network events for forensic analysis.

## Prerequisites
*   [Python 3.x](https://www.python.org/downloads/) (or your specific runtime)
*   Network interface with promiscuous mode support.
*   `libpcap` or `npcap` installed on the host machine.
*   Administrative / Root privileges (required for packet sniffing).

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ids-project.git
   ```
2. Navigate to the project directory:
   ```bash
   cd ids-project
   ```
3. (Optional) Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
4. Install necessary dependencies (e.g., Scapy):
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

Before running the IDS, you may need to define your detection rules and target network interface. 
Modify the `config.yaml` or `rules.txt` file in the root directory to set:
*   `interface`: The network interface to monitor (e.g., `eth0`, `wlan0`).
*   `log_level`: Detail of the output logs.
*   `alert_email`: (Optional) Email address for critical threat notifications.

## Usage

**Note:** You must run this application with elevated privileges to capture network traffic.

Run the main script from your terminal:

```bash
# On Linux / macOS
sudo python main.py --interface eth0

# On Windows (Run Command Prompt as Administrator)
python main.py --interface Ethernet
```

## Contributing
Contributions to improve threat detection rules, optimize performance, or add new features are welcome! Please feel free to submit a Pull Request or open an Issue.

## Disclaimer
This tool is for educational and authorized security monitoring purposes only. Ensure you have explicit permission to monitor the network traffic on your chosen interface.

## License
This project is licensed under the MIT License.