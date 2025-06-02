# Suricata-ELK-TheHive-Docs
This repository contains four plain-text files grouping installation and configuration commands for common open-source security tools.

1. **Elasticsearch & Kibana**   
2. **Suricata & Filebeat** 
3. **ElastAlert2**  
4. **TheHive & Cortex**


---

## Files and Their Contents

1. **`elasticsearch_kibana.txt`**  
   - Installs **Elasticsearch 8.x**, records the built-in `elastic` user password, and starts the service.  
   - Installs **Kibana**, generates an enrollment token, enrolls Kibana into the Elasticsearch cluster, and adjusts `kibana.yml`.
  
2. **`suricata_filebeat.txt`**  
   - Installs and configures **Suricata** (network IDS).  
   - Sets up a simple Suricata rule.  
   - Installs **Filebeat**, configures it to read Suricata’s JSON logs, and ships them to Elasticsearch.

3. **`elastalert.txt`**  
   - Installs **ElastAlert2** (Python 3.11 + virtual environment).  
   - Ensures the Elasticsearch client library is pinned to 7.x.  
   - Shows how to create the ElastAlert index in Elasticsearch and define a sample “Suricata ICMP Alert” rule that pushes alerts to TheHive.

4. **`thehive_cortex.txt`**  
   - Installs **Cassandra**, configures it for TheHive 4.  
   - Installs Elasticsearch (for use by TheHive).  
   - Installs **TheHive 4**, starts its service, and shows default admin credentials.  
   - Installs **Docker** (required by Cortex), pulls/runs the Cortex installer, and installs/pins required Python libraries for Cortex analyzers.  
   - Configures and starts the Cortex service.

---
