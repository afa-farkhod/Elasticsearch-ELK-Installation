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
  - Before running it, disable the security configuration in the following file, it is not necessary, but if you are having trouble to retrieve your password for elastic then it might be useful:  `c:\elastic-stack\elasticsearch-8.7.1\config\elasticsearch.yml` by making the configuration to `false`
 
  <p align="center">
    <img src="https://user-images.githubusercontent.com/24220136/236627245-7b96913a-51ef-4285-a644-85a204405fd1.png" alt="Image">
  </p>

  - Then go inside the following directory: `c:\elastic-stack\elasticsearch-8.7.1\bin` and run the command: `elasticsearch.bat`, then open the port: `localhost:9200` in the browser, you should see the following:

  <p align="center">
    <img src="https://user-images.githubusercontent.com/24220136/236627341-ada8ef31-851a-4dac-ae7f-9523bac9918e.png" alt="Image">
  </p>
