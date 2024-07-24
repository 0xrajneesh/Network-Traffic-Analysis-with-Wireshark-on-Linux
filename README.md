# Network Traffic Analysis with Wireshark on Linux

## Introduction

Network traffic analysis is a crucial skill for cybersecurity professionals. It involves capturing, inspecting, and understanding the packets of data that travel across a network. Wireshark is a powerful tool that allows users to capture and analyze network traffic in real-time. This lab will guide you through the process of using Wireshark on a Linux system to analyze network traffic, identify potential security issues, and understand network protocols.

## Pre-requisites

- Basic knowledge of networking concepts (IP addresses, protocols, etc.)
- Familiarity with Linux command-line interface
- Understanding of TCP/IP protocol suite

## Lab Set-up and Tools

- A computer running a Linux distribution (e.g., Ubuntu)
- Wireshark installed on the Linux system
- Internet connection for downloading necessary packages

### Installing Wireshark

1. Update your package list:
    ```bash
    sudo apt update
    ```
2. Install Wireshark:
    ```bash
    sudo apt install wireshark
    ```
3. Add your user to the `wireshark` group to capture packets without root privileges:
    ```bash
    sudo usermod -aG wireshark $(whoami)
    ```
4. Log out and log back in for the changes to take effect.

## Exercises

### Exercise 1: Capturing Network Traffic

**Objective**: Learn to capture live network traffic using Wireshark.

1. Open Wireshark.
2. Select the network interface to capture traffic from (e.g., `eth0` or `wlan0`).
3. Click the "Start Capturing Packets" button (blue shark fin).
4. Perform some network activities (e.g., browsing the web).
5. Stop the capture after a few minutes.
6. Observe the captured packets in Wireshark’s main window.

**Expected Output**: A list of captured packets with details such as source/destination IP, protocol, and length.

### Exercise 2: Applying Filters

**Objective**: Use Wireshark filters to narrow down and focus on specific types of traffic.

1. Start a new packet capture in Wireshark.
2. In the filter bar, type `http` to display only HTTP traffic.
3. Click "Apply" to filter the results.
4. Experiment with other filters like `tcp`, `ip.addr == <your_ip>`, and `dns`.
5. Observe how the displayed packets change based on the applied filters.

**Expected Output**: Filtered list of packets that match the criteria specified in the filter bar.

### Exercise 3: Analyzing HTTP Traffic

**Objective**: Examine HTTP packets to understand web traffic.

1. Start a new packet capture in Wireshark.
2. Open a web browser and visit a website.
3. Stop the packet capture.
4. Apply the `http` filter to display only HTTP traffic.
5. Select an HTTP GET request packet and inspect its details in the packet details pane.
6. Analyze the packet to understand the HTTP request headers and content.

**Expected Output**: Detailed view of an HTTP GET request with headers and content.

### Exercise 4: Identifying Malicious Traffic

**Objective**: Detect and analyze potential malicious traffic in a network capture.

1. Download a sample pcap file containing malicious traffic from a reputable source (e.g., Wireshark sample captures).
2. Open the pcap file in Wireshark.
3. Apply filters to identify suspicious activities, such as `tcp.port == 4444` (commonly used by malware).
4. Investigate the packets to determine the nature of the malicious activity.
5. Document your findings and the indicators of compromise (IOCs).

**Expected Output**: Identification of malicious packets and an understanding of their characteristics.

### Exercise 5: Extracting Files from Captures

**Objective**: Extract and analyze files transferred over the network.

1. Start a new packet capture in Wireshark.
2. Download a file from the internet during the capture.
3. Stop the packet capture.
4. Apply the `http` filter and locate the packets related to the file download.
5. Right-click on one of the packets and select "Follow" > "TCP Stream".
6. Save the file from the TCP stream for further analysis.

**Expected Output**: The extracted file from the network capture saved on your system.

## Conclusion

By completing these exercises, you have gained practical experience in capturing and analyzing network traffic using Wireshark on a Linux system. You have learned how to filter and examine packets, identify potential malicious activities, and extract files from network captures. These skills are essential for network security analysis and will aid you in detecting and responding to network-based threats.

## About Me

I am a cybersecurity trainer with a passion for teaching and helping others learn essential cybersecurity skills through practical, hands-on projects. Connect with me on social media for more updates and resources:

[![LinkedIn](https://img.icons8.com/fluent/48/000000/linkedin.png)](https://www.linkedin.com/in/rajneeshcyber)
[![YouTube](https://img.icons8.com/fluent/48/000000/youtube-play.png)](https://www.youtube.com/@rajneeshcyber)
[![Twitter](https://img.icons8.com/fluent/48/000000/twitter.png)](https://twitter.com/rajneeshcyber)

Feel free to reach out with any questions or feedback. Happy learning!
