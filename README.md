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
sudo apt-get update && sudo apt-get install openjdk-11-jdk

wget https://hyperledger.jfrog.io/artifactory/besu-binaries/besu/22.4.0-RC2/besu-22.4.0-RC2.zip
sudo apt-get install unzip
unzip besu-22.4.0-RC2.zip
```

Update the bashrc profile or 
```bash
export PATH=$PATH:~/besu-22.4.0-RC/bin
```

type besu --help to check if besu is installed properly
```bash
sudo apt install tree
mkdir Clique-network
cd Clique-network
```
Alternatily 

```bash
mkdir -p Clique-Network/{Node-1/{data},Node-2/{data},Node-3/{data}}
cd node1
~/besu-22.4.0-RC2/bin/besu --data-path=data public-key export-address --to=data/node1Address
```

Follow along using the tutorial.
https://besu.hyperledger.org/en/stable/Tutorials/Private-Network/Create-Private-Clique-Network/#1-create-directories
