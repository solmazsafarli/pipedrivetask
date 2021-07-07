## Pipedrivetask

# Instance Launch in AWS:

1. Create an account
2. Go to EC2 dashboard
3. Launch intance
4. Choose OS UBUNTU
5. Choose instance type (Note: the t2.medium has been selected)
6. Select the number of instances to launch (Note: we have created cluster of 3 nodes, which means that the number of instances is 3)
7. Indicate the storage
8. Configure security group (Note: type: All traffic)
9. Create key pair (Note: download)
10. View instance

# Deployment and Configuration of Elastic Stack

1. Open in terminal the IP addresses of created intances

For first instance
```bash
#ssh -i key.pem ubuntu@publicIPv4
ssh -i key.pem ubuntu@3.138.69.143 
```

For second instance
```bash
#ssh -i key.pem ubuntu@publicIPv4
ssh -i key.pem ubuntu@18.118.150.169 
```

For third instance
```bash
#ssh -i key.pem ubuntu@publicIPv4
ssh -i key.pem ubuntu@18.219.188.115 
```

Now we are in inside ubuntu

2. Set the environment

```bash
sudo apt-get update
sudo apt-get install -y openjdk-8-jdk
```

3. Download and extract packages

For elasticsearch
```bash
sudo wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.2.0-amd64.deb
sudo dpkg -i elasticsearch-7.2.0-amd64.deb
```

For Kibana
```bash
sudo wget https://artifacts.elastic.co/downloads/kibana/kibana-7.2.0-amd64.deb
sudo dpkg -i kibana-7.2.0-amd64.deb
```

For LogStash
```bash
sudo apt-get install -y apt-transport-https
sudo wget https://artifacts.elastic.co/downloads/logstash/logstash-7.2.0.deb
sudo dpkg -i logstash-7.2.0.deb
```

