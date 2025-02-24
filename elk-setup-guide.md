A beginner-friendly Elastic Stack (ELK) deployment guide for SOC labs.

# Elastic Stack (ELK) Setup for Threat Detection  

## Prerequisites  
- Ubuntu 22.04 LTS (4GB RAM minimum)  
- Elastic Cloud account (free tier)  

## Installation Steps  

### 1. Install Elasticsearch  
```bash  
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -  
sudo apt-get install apt-transport-https  
echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee /etc/apt/sources.list.d/elastic-7.x.list  
sudo apt-get update && sudo apt-get install elasticsearch  
sudo systemctl start elasticsearch  
```  

### 2. Configure Kibana  
```bash  
sudo apt-get install kibana  
sudo systemctl enable kibana  
sudo systemctl start kibana
```  

### 3. Ingest Logs with Filebeat  
```bash  
sudo apt-get install filebeat  
sudo filebeat modules enable system  
sudo filebeat setup --pipelines --modules system  
sudo systemctl start filebeat  
```  
