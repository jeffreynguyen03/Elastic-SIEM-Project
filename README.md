# Elastic-Siem-Project 

**[Work in Progress]**

This document provides a detailed account of the process I followed to build a home SIEM (Security Information and Event Management) lab using Elastic Stack, based on the tutorial I followed. The project involved setting up and configuring Elasticsearch, Logstash, and Kibana on a virtual machine, along with capturing network traffic using Packetbeat.

## Overview

The purpose of this project was to set up a fully functional SIEM lab to monitor and analyze security-related data from my home network. Using the Elastic Stack, I was able to collect, parse, and visualize log data, gaining insights into network activity and potential security threats.

## Prerequisites

Before starting this project, I ensured I had the following:

- A machine or VM running **Kali Linux** (preferably in **Oracle VirtualBox**)
- **Packetbeat** installed to capture network traffic
- Basic familiarity with Linux command-line operations
- A stable internet connection to download the necessary software packages

## Steps

1. **Set Up the Virtual Environment**
   - I created a Kali Linux virtual machine using Oracle VirtualBox.
   - Allocated appropriate resources (CPU, RAM, and disk space) to the VM for optimal performance.

2. **Installing and Configuring Elasticsearch**
   - Downloaded and installed Elasticsearch using the official package from Elastic.
   - Configured Elasticsearch by editing the `elasticsearch.yml` file to set network.host to `0.0.0.0` and ensure the service was accessible from outside the VM.
   - Started the Elasticsearch service and verified it was running correctly by accessing it via a web browser.

3. **Installing and Configuring Kibana**
   - Downloaded and installed Kibana.
   - Configured Kibana by editing the `kibana.yml` file to connect it to the Elasticsearch instance.
   - Started the Kibana service and accessed the Kibana web interface to ensure it was properly connected to Elasticsearch.

4. **Installing and Configuring Logstash**
   - Downloaded and installed Logstash.
   - Created a Logstash configuration file to define input, filter, and output settings. This involved setting up Filebeat as the input and Elasticsearch as the output.
   - Tested the Logstash configuration to ensure logs were being correctly ingested and processed.

5. **Setting Up Packetbeat**
   - Installed Packetbeat on the Kali Linux VM to monitor and collect network traffic data.
   - Configured Packetbeat to capture network packets and send the data to Elasticsearch.
   - Verified that Packetbeat was correctly capturing and sending data to Elasticsearch by checking the indices in Kibana.

6. **Creating Dashboards and Visualizations in Kibana**
   - Accessed the Kibana interface and used the data ingested from Logstash and Packetbeat to create custom visualizations and dashboards.
   - These visualizations provided insights into network traffic patterns and potential security threats.

7. **Testing and Verifying the Setup**
   - I performed various network activities to generate traffic and logs, ensuring that all components (Elasticsearch, Logstash, Kibana, and Packetbeat) were functioning correctly.
   - I monitored the data flow and validated that the visualizations in Kibana accurately reflected the network activity.

## Skills Learned

Through this project, I developed the following skills:

- **Elastic Stack Configuration:** Gained experience in setting up, configuring, and troubleshooting Elasticsearch, Logstash, and Kibana.
- **Network Traffic Analysis:** Learned to use Packetbeat to capture and analyze network traffic in real-time.
- **Log Management and Parsing:** Improved my ability to work with Logstash for log ingestion and parsing.
- **SIEM Concepts:** Developed a deeper understanding of Security Information and Event Management (SIEM) principles and how to apply them using Elastic Stack.
- **Linux Command-Line Proficiency:** Enhanced my skills in managing Linux services and configurations via the command line.

## Conclusion

Completing this project provided me with valuable hands-on experience in setting up and using a SIEM system with Elastic Stack. The steps followed allowed me to monitor network activity and analyze security-related data effectively in a home lab environment.
