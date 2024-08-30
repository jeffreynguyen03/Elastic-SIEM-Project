# Elastic-Siem-Project

**[Status: Work in Progress]**

This document provides a detailed account of the process I followed to build a home SIEM (Security Information and Event Management) lab using Elastic Stack. The project involved installing, configuring, and testing Elasticsearch and Kibana on a Kali Linux virtual machine.

## Overview

The purpose of this project was to set up a fully functional SIEM lab to monitor and analyze security-related data from my home network. Using the Elastic Stack, I was able to collect, parse, and visualize log data, gaining insights into network activity and potential security threats.

## Prerequisites

Before starting this project, I ensured I had the following:

- A machine or VM running **Kali Linux** (preferably in **Oracle VirtualBox**)
- **Packetbeat** installed to capture network traffic
- **Elastic Stack** components (Elasticsearch, Kibana) installed
- Basic familiarity with Linux command-line operations

## Steps

1. **Installing and Configuring Elasticsearch**
   - Downloaded and installed Elasticsearch using the official package from Elastic.
   - Configured Elasticsearch by editing the `elasticsearch.yml` file to set network.host to `0.0.0.0` and ensure the service was accessible from outside the VM.
   - Started the Elasticsearch service and verified it was running correctly by accessing it via a web browser.

2. **Installing and Configuring Kibana**
   - Downloaded and installed Kibana.
   - Configured Kibana by editing the `kibana.yml` file to connect it to the Elasticsearch instance.
   - Started the Kibana service and accessed the Kibana web interface to ensure it was properly connected to Elasticsearch.

3. **Installing and Configuring Packetbeat**
   - Installed Packetbeat on the Kali Linux VM to monitor and collect network traffic data.
   - Configured Packetbeat to capture specific network protocols (like HTTP, DNS) and send the data directly to Elasticsearch.
   - Verified that Packetbeat was correctly capturing and sending data to Elasticsearch by checking the indices in Kibana.

4. **Testing and Verifying the Setup**
   - Performed various network activities to generate traffic and logs.
   - Used Kibana to visualize and analyze the network data captured by Packetbeat, ensuring that all components were functioning correctly.

## Skills Learned

Through this project, I developed the following skills:

- **Elastic Stack Configuration:** Gained experience in setting up, configuring, and troubleshooting Elasticsearch and Kibana.
- **Network Traffic Analysis:** Learned to use Packetbeat to capture and analyze network traffic in real-time.
- **SIEM Concepts:** Developed a deeper understanding of Security Information and Event Management (SIEM) principles and how to apply them using Elastic Stack.
- **Linux Command-Line Proficiency:** Enhanced my skills in managing Linux services and configurations via the command line.

## Conclusion

Completing this project provided me with valuable hands-on experience in setting up and using a SIEM system with Elastic Stack. The steps followed allowed me to monitor network activity and analyze security-related data effectively in a home lab environment.

