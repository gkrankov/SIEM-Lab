# 🔍 SIEM Log Analysis & SOC Labs  
*A hands-on repository showcasing SIEM deployments, log analysis, and threat detection workflows for aspiring SOC Analysts.*  

[![Elastic Stack](https://img.shields.io/badge/Elastic-Stack-005571?logo=elasticstack)](https://www.elastic.co/)
[![Splunk](https://img.shields.io/badge/Splunk-SPL-%23000000?logo=splunk)](https://www.splunk.com/)
[![Wireshark](https://img.shields.io/badge/Wireshark-PCAPs-1679B5?logo=wireshark)](https://www.wireshark.org/)

---

## 🛠️ Repository Contents  
This repository demonstrates practical SOC skills through:  
- **SIEM (Elastic Stack) deployment guides**  
- **Real-world log analysis** (PCAPs, firewall logs)  
- **Splunk SPL detection queries**  
- **Visual threat-hunting workflows**  

---

## 📂 Repository Structure  

📁 SIEM-Log-Analysis  
├── 📄 README.md                      # Overview of the repository (you're here!)  
├── 📁 elk-setup-guide                # Elastic Stack deployment tutorials  
│   ├── 📄 elk-setup-guide.md         # Step-by-step Elastic Stack installation  
│   └── 📄 elk-demo-lab.md            # Sample lab: Brute-force attack detection  
├── 📁 sample-logs                    # Real-world logs and PCAPs for analysis  
│   ├── 📄 ssh-brute-force.pcap       # PCAP of brute-force attempts  
│   └── 📄 phishing-email-logs.json   # Sample email gateway logs  
├── 📁 splunk-queries                 # Splunk SPL for SOC use cases  
│   ├── 📄 suspicious-logins.spl      # Detect anomalous sign-ins  
│   └── 📄 malware-c2-alerts.spl      # Identify C2 traffic patterns  
└── 📁 screenshots                    # Visual evidence of your work  
    ├── 📄 kibana-dashboard.png       # SIEM dashboard for brute-force attacks  
    └── 📄 wireshark-analysis.png     # Tagged malicious traffic in Wireshark  


---

## 🚀 **ELK Stack Setup Guide**  
*Deploy Elasticsearch, Kibana, and Filebeat to detect brute-force attacks.*  

### Step-by-Step Summary:  
1. **Install Elasticsearch**  
   ```bash  
   sudo apt-get install elasticsearch  
   systemctl start elasticsearch  
   ```
   
2. **Configure Kibana**  
   ```bash  
   sudo apt-get install kibana  
   systemctl enable kibana   
   ```
   
3. **Ingest Logs with Filebeat**  
  ```bash  
  filebeat modules enable system  
  filebeat setup --pipelines --modules system    
   ```
