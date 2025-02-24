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
