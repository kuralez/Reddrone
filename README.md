# 🛡️ Securing Autonomous Drones

A cybersecurity-focused project that explores the vulnerabilities of autonomous drones and implements mitigation strategies. This project demonstrates real-world cyberattack scenarios on drones using Wi-Fi networks, followed by recommendations for securing communication channels.

## 📚 Project Overview

Autonomous drones rely heavily on wireless communication for navigation, telemetry, and control. This project identifies potential attack vectors and proposes countermeasures to improve drone cybersecurity.

- 🔍 Focus Areas:
  - Drone reconnaissance and traffic analysis
  - Exploitation of insecure communication protocols (e.g., MAVLink)
  - Reverse engineering mobile applications
  - Drone hijacking and video feed capture
  - MAC address spoofing for access bypass

## ⚔️ Attack Scenarios

The list of attack scenarios below is organized by attack stages. Note that some attacks are only possible during certain drone flight states.

| Reconnaissance           | Protocol Tampering       | Denial of Service          | Injection                    | Exfiltration               | Firmware Attacks       |
|--------------------------|---------------------------|-----------------------------|-------------------------------|----------------------------|------------------------|
| WiFi Analysis & Cracking | Telemetry Spoofing        | Battery Drain Attack        | MAVLink Command Injection     | Flight Log Extraction      | Firmware Decompile     |
| Drone Discovery           | Flight Mode Spoofing      | Communication Link Flooding | Camera Gimbal Takeover        | Parameter Extraction       | Firmware Modding       |
| Packet Sniffing           | Drone State Spoofing      | Denial-of-Takeoff           | Waypoint Injection            | Mission Extraction         |                        |
| Protocol Fingerprinting   | GPS Spoofing              | Geo-Squeezing               | Sensor Data Injection         | FTP Eavesdropping          |                        |
| GPS & Telemetry Analysis  |                           | Altitude Limiting           | Flight Mode Injection         | Camera Feed Eavesdropping  |                        |
| Payload Detection         |                           | GPS Jamming                 |                               |                            |                        |
| **Wireless Deauthentication** |                        |                             |                               |                            |                        |

---

## 🔍 Key Findings

- ✅ **Wireless Deauthentication Attack** successfully performed to disconnect the drone from its ground control station.
- 🧠 **Reverse-engineered the drone's mobile application** to analyze authentication and telemetry endpoints.
- 🎭 **Cloned the MAC address** to bypass MAC filtering and hijack the connection.
- 📹 **Drone Hijacking Achieved**: Full access was gained to the drone, including live video feed capture and basic navigation override.

## 🧰 Tools Used

- Kali Linux
- Aircrack-ng
- Wireshark
- Bettercap
- MITMf
- ESP8266 (Wi-Fi module)
- ApkTool / JADX for APK reverse engineering

## 🧭 Architecture Diagram

![CYS 10 Poster](https://github.com/user-attachments/assets/6b696e08-50d6-4a93-ac8c-2f78b5880bfb)


## 🛡️ Mitigation Strategies

- Enforce WPA3 encryption
- Implement certificate-based mutual authentication
- Use MAC address whitelisting with anomaly detection
- Monitor drone network activity with IDS tools
- Harden firmware with signed updates and validation
- Secure the MAVLink protocol with encryption and validation
- Restrict drone control access to trusted devices

## 📌 Future Scope

- Integration of AI/ML-based anomaly detection for drone traffic
- Use of blockchain for secure telemetry and mission logging
- Exploration of SDR (Software Defined Radio) attacks and defenses
- Legislative compliance study for autonomous aerial security

## 👤 Author

**Kuralamudhan**   
Passionate about drone security, ethical hacking, and VAPT.

**Vigneshwaran**  
Passionate about drone security, ethical hacking, and VAPT.

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.
