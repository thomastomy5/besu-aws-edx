# besu-aws-edx. 

Create an instance with security group :sg-002ed640d5dd8a2da: (launch-wizard-4). \
\
With inbound rules as below. Or can choose the security group mentioned above. sorry folks the above mentioned security group is availble only for me you need to manually enter the details or you can use terraforms. In the next update I will try to include the teraforms files so that you can start the aws instance with zero mouse clicks. IsIn't it a good propostion.  
Port 22 : TCP for SSH. \
port : 30303 UDP \
below mentioned ports are all TCP \
8547,8545, 30303, 8546, 9545. \
After instance starts, SSH into it.


```bash
echo 'ClientAliveInterval 60' | sudo tee --append /etc/ssh/sshd_config
ubuntu
sudo service ssh restart
any other linux
sudo service sshd restart
```

```bash
sudo apt-get update && sudo apt-get install openjdk-11-jdk

wget https://hyperledger.jfrog.io/artifactory/besu-binaries/besu/22.4.0-RC2/besu-22.4.0-RC2.zip
sudo apt-get install unzip
unzip besu-22.4.0-RC2.zip
```

```bash
rm -r besu-22.4.0-RC2.zip
mv besu-22.4.0-RC2 besu
```

Update the bashrc profile or 
```bash
export PATH=$PATH:~/besu/bin
```

type besu --help to check if besu is installed properly
```bash
sudo apt install tree
```

```bash
mkdir -p Clique-Network/{node-1/data,node-2/data,node-3/data}
cd node1
~/besu/bin/besu --data-path=data public-key export-address --to=data/node1Address
```

Follow along using the tutorial.
https://besu.hyperledger.org/en/stable/Tutorials/Private-Network/Create-Private-Clique-Network/#1-create-directories

touch cliqueGenesis.json
vim cliqueGenesis.json

Install Grafana 
https://www.muvi.com/blogs/install-grafana-on-ec2-and-start-with-an-autostart-for-monitoring.html
