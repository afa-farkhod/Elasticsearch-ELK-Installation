# [Elastic-Stack-Installation](https://www.elastic.co/guide/en/elastic-stack/current/installing-elastic-stack.html)
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

- [Download Kibana](https://www.elastic.co/kr/downloads/kibana) <tr><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3_RqXgpJRFZ-5KPzNMyzWJaJxwXERWjSxjA&usqp=CAU" width="30" title=""></tr>
  - You can choose OS type: Windows, macOS, Linux.
  - Also can choose packages: yum, dnf, zypper, apt-get
  - You can run in `Docker` container
  - Go inside the following directory: `c:\elastic-stack\kibana-8.7.1\bin` then run the command: `kibana.bat`, there is nothing to make changes in the configuration files. Just open the port: `localhost:5601` in browser, then you can see Kibana interface is running:

  <p align="center">
    <img src="https://user-images.githubusercontent.com/24220136/236627447-8d64ffa1-f6f0-41f1-bbc6-73c9a5e791a8.png" alt="Image">
  </p>

- [Download Logstash](https://www.elastic.co/kr/downloads/logstash) <tr><img src="https://elastic-content-share.eu/wp-content/uploads/edd/2020/06/logstash-logo-color.png" width="35" title=""></tr>
  - You can choose OS type: Windows, macOS, Linux.
  - Also can choose packages: yum, apt-get
  - You can run in `Docker` container
  - Logstash is basically used as the pipeline to ingest the data to elasticsearch. So in the following we get sample from `kaggle.com` dataset website, the following is the sample dataset `flowers.csv`:

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236627845-e8a5fa86-e5e9-4760-9010-8bdaeecd7fa2.png" alt="Image">
</p>

   - So now we create `logstash.conf` file, and show the dataset location to ingest to elasticsearch. Before, in `flowers.csv` file we have to show the following columns: 

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236627979-41abeadb-4218-4025-81bd-c8b8500e121e.png" alt="Image">
</p>

   - Following is the `logstash.conf` file with the dataset path and columns names:

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236628145-12d9bdf1-b7b2-45a8-b9e8-2ad997435924.png" alt="Image">
</p>

   - To ingest the data, we have to be in a folder where our `logstash.conf` file is located. Then run the following command: `logstash -f logstash.conf`

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236628258-5b135b2c-93d9-4627-a994-123f6bb039d9.png" alt="Image">
</p>

   - Then in Kibana interface we go to Dev Tools and can check our ingested data: 

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236628339-81aa632a-ad9c-4be2-b10b-652b752b52c2.png" alt="Image">
</p>

-----------------

### [Elasticsearch on Linux](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-22-04)

- We can also run the Elasticsearch, Kibana and Logstash at once inside the `docker-compose.yml` file based on `Linux` Operating System:
- Following is the `Elasticsearch` container by pulling the `elasticsearch:7.16.2` image from the Docker hub:

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236646804-424bf108-ac1f-4a7c-a125-160caa1dfdd8.png" alt="Image">
</p>

- Following is `Kibana` container by pulling the `kibana:7.16.2` image from the Docker hub:

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236646816-7c0ba095-3333-42e8-ab97-72d835a7a730.png" alt="Image">
</p>

- Following is `Logstash` container by pulling the `logstash:7.16.2` image from the Docker hub:

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236646902-52215f82-5c92-4b25-ada7-b8adaa824350.png" alt="Image">
</p>

- Then we bring them all inside the `docker-compose.yml` file which runs the elasticsearch inside the docker container. To do so we run the command `docker-compose.up`:

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/227846350-d2fc6be7-e676-4dd4-9038-ba248b6e67f3.png" alt="Image">
</p>

- We can see our running servers inside the docker containers with the following command:

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/227846458-ea87f3dd-fc05-4904-b5e4-7ae8544d99b6.png" alt="Image">
</p>

- We can check elasticsearch on port:9200 (if you pay attention to cluster_name: "docker-cluster")

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/227846675-a1fc845e-7bb8-4bf5-8d64-19c5ebed703e.png" alt="Image">
</p>

-------------------------

- Don't forget to set environmental variables as following in the beginning!:

<p align="center">
  <img src="https://user-images.githubusercontent.com/24220136/236627530-518d74a9-fb68-4317-b4ec-bd9dbc0b4a34.png" alt="Image">
</p>
