# Cybersecurity Internship — Week 2

## Footprinting, Reconnaissance & Network Scanning

**Cybersecurity & Ethical Hacking Internship — NETWORKWALKS**

---

## 📌 Internship Information

| Field            | Details                                                              |
| ---------------- | -------------------------------------------------------------------- |
| **Intern Name**  | Sobia Manzoor                                                        |
| **Batch**        | B083                                                                   |
| **Program**      | Cybersecurity & Ethical Hacking Internship                           |
| **Organization** | NETWORKWALKS                                                         |
| **Week**         | Week 2                                                               |
| **Focus Areas**  | Footprinting, Web Reconnaissance, DNS Enumeration & Network Scanning |
| **Status**       | ✅ Completed                                                          |

---

## 📖 Introduction

This README documents the practical work I completed during **Week 2 of my Cybersecurity & Ethical Hacking Internship at NETWORKWALKS**.

The week focused on understanding the **reconnaissance and network discovery phases** of cybersecurity. I practically worked with different command-line tools and Zenmap to collect domain information, identify web technologies, resolve IP addresses, inspect HTTP headers, detect Web Application Firewall (WAF) presence, enumerate DNS records, and discover live hosts on an authorized local network.

All tasks were performed for **educational and internship purposes within an authorized scope**. No exploitation or destructive activity was performed.

---

# 🛠️ Tools Used

| Tool                       | Purpose                                                                              |
| -------------------------- | ------------------------------------------------------------------------------------ |
| `whois`                    | Used to obtain domain registration and ownership-related information.                |
| `whatweb`                  | Used to identify technologies and software associated with a website.                |
| `nslookup`                 | Used to resolve a domain name to its IP address.                                     |
| `curl -I`                  | Used to inspect HTTP response headers.                                               |
| `wafw00f`                  | Used to detect the presence of a Web Application Firewall.                           |
| `dnsrecon`                 | Used to enumerate DNS records and gather DNS-related information.                    |
| **Zenmap**                 | Graphical interface for Nmap, used for network discovery and topology visualization. |
| **Windows Command Prompt*1| Used to identify the local IP address and subnet information.                        |

---

# 🔍 Tasks Performed

## Task 1 — WHOIS Domain Registration Lookup

### Objective

To obtain publicly available domain registration information using WHOIS.

### Command Used

```bash
whois networkwalks.com
```

### Practical Work

I ran the WHOIS command to retrieve domain registration details, including registrar information, domain dates, name servers, DNSSEC status, and domain status.

### Evidence

<img width="1920" height="891" alt="Screenshot_2026-09-16_04_07_52" src="https://github.com/user-attachments/assets/b53ce8ab-0cb8-4693-85e4-debc60a5204c" />


*Figure 1 — WHOIS command showing domain registration information.*

---

## Task 2 — WhatWeb Web Technology Fingerprinting

### Objective

To identify the technologies and software components associated with the target website.

### Command Used

```bash
whatweb networkwalks.com
```

### Practical Work

I used WhatWeb to fingerprint the website and identify technologies such as the CMS, plugins, JavaScript libraries, web server, and other detectable components.

### Evidence

<img width="1920" height="891" alt="Screenshot_2026-09-16_04_51_15" src="https://github.com/user-attachments/assets/64164b70-35c9-41f8-8fe4-a9557228baf2" />


*Figure 2 — WhatWeb output showing detected web technologies.*

---

## Task 3 — NSLookup Domain Resolution

### Objective

To resolve the domain name and identify its associated IP address.

### Command Used

```bash
nslookup networkwalks.com
```

### Practical Work

I used NSLookup to perform DNS resolution and identify the IP address associated with the domain.

### Evidence

<img width="1920" height="891" alt="Screenshot_2026-09-16_04_53_01" src="https://github.com/user-attachments/assets/cc3bc9a1-986e-44ba-b25f-a1a8c205b81f" />


*Figure 3 — NSLookup output showing domain-to-IP resolution.*

---

## Task 4 — HTTP Response Headers Using cURL

### Objective

To inspect the HTTP response headers returned by the website.

### Command Used

```bash
curl -I https://networkwalks.com
```

### Practical Work

I used the `curl -I` command to retrieve the HTTP response headers without downloading the complete webpage.

This helped me observe information provided through HTTP headers, including server-related and security-related header information.

### Evidence

<img width="1920" height="891" alt="Screenshot_2026-09-16_04_56_30" src="https://github.com/user-attachments/assets/65556e61-a500-4d17-b671-2c85ae0b3bdc" />


*Figure 4 — cURL HTTP response header output.*

---

## Task 5 — WAF Detection Using Wafw00f

### Objective

To determine whether a Web Application Firewall was present in front of the target website.

### Command Used

```bash
wafw00f networkwalks.com
```

### Practical Work

I used Wafw00f to check whether the target website was protected by a Web Application Firewall and to identify the detected WAF technology.

### Evidence

<img width="1920" height="891" alt="Screenshot_2026-09-16_04_58_43" src="https://github.com/user-attachments/assets/62358a6e-ae8b-4352-930b-0d1ceced8c9b" />


*Figure 5 — Wafw00f output showing WAF detection.*

---

## Task 6 — DNS Enumeration Using DNSRecon

### Objective

To enumerate DNS records associated with the target domain.

### Command Used

```bash
dnsrecon -d networkwalks.com
```

### Practical Work

I used DNSRecon to gather DNS-related information, including available **SOA, NS, MX, TXT/SPF and SRV records**.

This provided practical experience in understanding how DNS information can contribute to the reconnaissance phase of a security assessment.

### Evidence

<img width="1920" height="891" alt="Screenshot_2026-09-16_05_02_00" src="https://github.com/user-attachments/assets/c9bd68e5-966c-47c7-9208-68a44762e2f4" />


*Figure 6 — DNSRecon output showing discovered DNS records.*

---

# 🖥️ Network Scanning with Zenmap

The second part of my practical work focused on **local network discovery using Zenmap**.

Zenmap is the graphical user interface for Nmap and can be used to discover active hosts and visualize network topology.

---

## Task 7 — Download & Install Zenmap

### Objective

To install Zenmap on my Windows PC for network scanning and host discovery.

### Practical Work

I downloaded and installed Zenmap and prepared it for the network scanning activity.

### Evidence

<img width="960" height="540" alt="Screenshot 2026-09-16 121256" src="https://github.com/user-attachments/assets/1ba32297-5156-4e1e-8d3e-529cd0d24111" />
<img width="960" height="540" alt="Screenshot 2026-09-16 121745" src="https://github.com/user-attachments/assets/ede2d1f4-8d07-421f-9e56-631d526d5a82" />


*Figure 7 — Zenmap installed and ready for use.*

---

## Task 8 — Find Local IP Address & LAN Subnet

### Objective

To identify my local IPv4 address and determine the LAN subnet before performing the network scan.

### Command Used

```cmd
ipconfig
```

### Practical Work

I used Windows Command Prompt to identify the local network configuration, including the IPv4 address and subnet mask.

### Evidence

<img width="960" height="540" alt="Screenshot 2026-09-17 022458" src="https://github.com/user-attachments/assets/a765c596-808f-42b0-8d0f-e5f5a1f766f5" />


*Figure 8 — Local IPv4 address and subnet information.*

---

## Task 9 — Find Live Hosts in the IP Subnet

### Objective

To discover which hosts were active within the identified subnet.

### Scan Used

```bash
nmap -sn 192.168.0.0/24>
```

### Practical Work

I configured Zenmap with my local subnet and performed a **Ping Scan** to identify responding/live hosts.

The scan was performed within my authorized local network environment.

### Evidence

<img width="960" height="540" alt="Screenshot 2026-09-16 122814" src="https://github.com/user-attachments/assets/68563242-783b-43bf-a456-9b6ce5f3edc3" />


*Figure 9 — Zenmap configured for the local subnet and Ping Scan.*

---

## Task 10 — Determine the Number of Live Hosts

### Objective

To determine how many hosts responded during the network scan.

### Result
"The scan identified 4 active hosts within the scanned subnet."
The scan results showed the number of active hosts responding within the scanned subnet.

### Evidence

<img width="960" height="540" alt="Screenshot 2026-09-16 122719" src="https://github.com/user-attachments/assets/c0d37d28-05eb-469f-a1b7-0f3a0972708c" />

*Figure 10 — Zenmap scan result showing the live hosts.*

---

## Task 11 — Identify IP Addresses of Live Hosts

### Objective

To identify the IP addresses of the hosts discovered during the scan.

### Evidence

<img width="960" height="540" alt="Screenshot 2026-09-16 122234" src="https://github.com/user-attachments/assets/058c2c77-7769-4800-8b4f-771aefbaa8e6" />

*Figure 11 — IP addresses of the discovered live hosts.*

---

## Task 12 — Identify MAC Addresses of Live Hosts

### Objective

To identify the MAC addresses associated with the discovered hosts where available.

### Result

192.168.0.108 → 02:41:09:57:C8:2E
192.168.0.139 → 00:08:22:6C:F2:FB
192.168.0.254 → 08:40:F3:0F:4B:98

The MAC address information was reviewed from the network scan results.

### Evidence

<img width="1920" height="891" alt="VirtualBox_kali-linux-2026 2-virtualbox-amd64_09_09_2026_02_41_46" src="https://github.com/user-attachments/assets/9603c92e-8772-471c-959a-eb2c0211f2a7" />
<img width="1920" height="891" alt="VirtualBox_kali-linux-2026 2-virtualbox-amd64_09_09_2026_02_40_53" src="https://github.com/user-attachments/assets/1922cfa7-285d-4cbd-a719-d37552c441e1" />

*Figure 12,13 — MAC addresses of the discovered hosts.*

Task 13 — Display & Save Network Topology
Objective

To visualize the discovered network hosts using Zenmap's topology feature and save the topology output in PDF format.

Practical Work

After completing the network scan, I reviewed the Topology section in Zenmap to visualize the discovered network structure.

I then saved the topology output in PDF format as required for the practical task.

Evidence

<img width="587" height="405" alt="Screenshot 2026-09-17 121024" src="https://github.com/user-attachments/assets/6e82dcf0-d8e1-4481-82b7-66b20b7bad0f" />


Figure 14 — Zenmap topology view showing the discovered network.

---


# 📊 Practical Results Summary

| Area           | Practical Activity                   | Status      |
| -------------- | ------------------------------------ | ----------- |
| WHOIS          | Domain registration lookup           | ✅ Completed |
| WhatWeb        | Web technology fingerprinting        | ✅ Completed |
| NSLookup       | Domain-to-IP resolution              | ✅ Completed |
| cURL           | HTTP response header analysis        | ✅ Completed |
| Wafw00f        | WAF detection                        | ✅ Completed |
| DNSRecon       | DNS record enumeration               | ✅ Completed |
| Zenmap         | Installation and network scanning    | ✅ Completed |
| Local Network  | IP address and subnet identification | ✅ Completed |
| Host Discovery | Live host identification             | ✅ Completed |
| IP Discovery   | Live host IP addresses               | ✅ Completed |
| MAC Discovery  | Live host MAC addresses              | ✅ Completed |
| Topology       | Network topology visualization       | ✅ Completed |
| PDF            | Topology saved in PDF format         | ✅ Completed |

---

# 💡 Key Learning Outcomes

Through these practical activities, I gained hands-on experience in:

* Understanding the **reconnaissance phase** of cybersecurity.
* Collecting domain registration information using WHOIS.
* Identifying website technologies using WhatWeb.
* Performing DNS resolution using NSLookup.
* Reading HTTP response headers using cURL.
* Understanding WAF detection using Wafw00f.
* Enumerating DNS records using DNSRecon.
* Using Zenmap for practical network discovery.
* Identifying local IP addresses and subnet information.
* Discovering live hosts within an authorized network.
* Reviewing IP and MAC address information.
* Creating and saving a network topology.

These exercises helped me understand how basic reconnaissance and network discovery techniques can provide useful information about a system or network before deeper security testing begins.

---

# 🔐 Scope & Authorization

All activities documented in this repository were performed for **educational and internship purposes within an authorized scope**.

The domain reconnaissance activities were performed as part of the authorized internship exercise, while the network scanning activities were performed within my local/authorized network environment.

No unauthorized systems were intentionally targeted, and no exploitation or destructive activity was performed.

> **Important:** Security scanning and reconnaissance should only be performed against systems and networks for which explicit authorization has been provided.

---

# 📸 Evidence

Screenshots captured during the practical activities are included throughout this README.

### Evidence Included

1. WHOIS output
2. WhatWeb output
3. NSLookup output
4. cURL HTTP headers
5. Wafw00f output
6. DNSRecon output
7. Zenmap installation
8. Local IP/subnet information
9. Zenmap scan configuration
10. Live host scan results
11. IP address results
12. MAC address results
13. Zenmap topology
14. Network topology PDF
--

# 📁 Repository Structure

```text
Week-2-Cybersecurity/
│
├── README.md
│
├── Screenshots/
│   ├── fig1-whois.png
│   ├── fig2-whatweb.png
│   ├── fig3-nslookup.png
│   ├── fig4-curl.png
│   ├── fig5-wafw00f.png
│   ├── fig6-dnsrecon.png
│   ├── fig7-zenmap-installation.png
│   ├── fig8-ipconfig.png
│   ├── fig9-zenmap-scan.png
│   ├── fig10-zenmap-result.png
│   ├── fig11-live-hosts.png
│   ├── fig12-mac-addresses.png
│   └── fig13-zenmap-topology.png
│
└── Network_Topology.pdf
```

---

# ✅ Conclusion

Week 2 provided practical exposure to the **reconnaissance, footprinting, DNS enumeration, and network discovery** stages of cybersecurity.

By performing these tasks myself, I developed a better understanding of how different tools can be used together to gather technical information about a domain and discover active hosts within an authorized network.

The practical work also helped me strengthen my familiarity with **Kali Linux command-line tools, Windows networking commands, Zenmap, DNS concepts, web technologies, and basic network security practices**.

This hands-on experience has provided a strong foundation for understanding the next stages of cybersecurity and ethical security assessment.

---

## 👤 Author

**Sobia Manzoor**

**Batch:** B083
**Program:** Cybersecurity & Ethical Hacking Internship
**Organization:** NETWORKWALKS

---

### 🔗 LinkedIn

https://www.linkedin.com/posts/sobia-manzoor-672552425_cybersecurity-ethicalhacking-footprinting-activity-7506095859567345664-7Bvo?utm_source=share&utm_medium=member_desktop&rcm=ACoAAGvB8jYBelji3Uy1ICJ4GbQcpWhERU9sULo


