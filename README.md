# Elastic-Stack-Installation
Elastic Stack Installation: Elasticsearch, Kibana and Logstash. 

### [Elastic stack installation guide:](https://www.elastic.co/guide/en/elastic-stack/current/installing-elastic-stack.html)

- When installing the Elastic Stack, you must use the same version across the entire stack. For example, if you are using `Elasticsearch 8.8.2`, you install `Beats 8.8.2`, `APM Server 8.8.2`, `Elasticsearch Hadoop 8.8.2`, `Kibana 8.8.2`, and `Logstash 8.8.2`.
- [Installation Order](https://www.elastic.co/guide/en/elastic-stack/current/installing-elastic-stack.html#install-order-elastic-stack)
  - Install the Elastic Stack products you want to use in the following order:
    - Elasticsearch
    - Kibana
    - Logstash
    - Beats
    - APM
    - Elasticsearch Hadoop
- [Beginner's Crash Course to Elastic Stack](https://youtu.be/gS_nHTWZEJ8) - Official Elastic Community. Beginner’s Crash Course is a series of workshops for all developers with little to no experience with Elasticsearch and Kibana or those who could use a refresher. By the end of this workshop, you will be able to: 
  - understand how the products of Elastic Stack work together to search, analyze, and visualize data in real time
  - understand the basic architecture of Elasticsearch
  - run CRUD operations with  Elasticsearch and Kibana
 
- [Download Elasticsearch](https://www.elastic.co/downloads/elasticsearch) <tr><img src="https://edent.github.io/SuperTinyIcons/images/svg/elastic.svg" width="35" title=""></tr>
  - You can choose OS type: Windows, macOS, Linux.
  - Also can choose packages: yum, dnf, zypper, apt-get
  - You can run in `Docker` container
  - After downloading the `Elasticsearch` run the following command to start the Elasticsearch server
    ```
    bin/elasticsearch.bat
    ```
