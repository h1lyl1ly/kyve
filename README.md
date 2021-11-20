# kyve
## Preparing to install

1. Open metamask and add **Moonbase Alpha**
```
Network Name: Moonbase Alpha
RPC URL: https://rpc.testnet.moonbeam.network
ChainID: 1287
Symbol: DEV
Block Explorer: https://moonbase-blockscout.testnet.moonbeam.network
```

2. Add token KYVE. Contract: **0xb5e10F806e86b7d2415c126d8864032f12325BBE**
3. Open https://app.kyve.network/faucet
4. Click on share on twitter
5. Add you link with share twitter and click "Claim your tokens"

# install
## 1 CPU x 2 GB RAM x 40 GB SSD (requirements)
```
sudo apt-get update && sudo apt-get upgrade -y
```
**Docker install (one command)**
```
sudo apt-get install curl gnupg apt-transport-https ca-certificates \
lsb-release -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg \
| sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
echo "deb [arch=$(dpkg --print-architecture) \
signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" \
| sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt-get update && \
sudo apt-get install docker-ce docker-ce-cli containerd.io -y
```
**Up the docker**
```
sudo systemctl start docker && sudo systemctl enable docker
```

**NOTE**

In the commands below you need to replace 2 variables:

<PK> - to the private key from the metamask (where DEV and KYVE were requested);
<amount> - to the desired number of tokens (I recommend from 11 to 990, a smaller or larger number may cause an error).

**Up avalanche (one command)**
  
```
docker pull kyve/evm:v0.0.11 && \
docker stop kyve-avalanche-node 2>/dev/null; \
docker container rm kyve-avalanche-node 2>/dev/null; \
docker run -d -it --restart=always \
--name kyve-avalanche-node kyve/evm:v0.0.11 \
--pool 0xd1EAe9CC4C0cC8D82c5800e2dAE972A70f2C4d0d \
--private-key <PK> \
--stake <amount> \
-e https://rpc.testnet.moonbeam.network
```
**Up moonriver (one command)**
```
docker pull kyve/evm:v0.0.11 && \
docker stop kyve-moonriver-node 2>/dev/null; \
docker container rm kyve-moonriver-node 2>/dev/null; \
docker run -d -it --restart=always \
--name kyve-moonriver-node kyve/evm:v0.0.11 \
--pool 0x5A679d476757C18Ec49dfB6c3c3511c8E8a76906 \
--private-key <PK> \
--stake <amount> \
-e https://rpc.testnet.moonbeam.network
```
**Up cosmos (one command)**
```
docker pull kyve/cosmos:v0.0.0 && \
docker stop kyve-cosmos-node 2>/dev/null; \
docker container rm kyve-cosmos-node 2>/dev/null; \
docker run -d -it --restart=always \
--name kyve-cosmos-node kyve/cosmos:v0.0.0 \
--pool 0x83748889798a93e4a816a6a9D2ecD40377D5530B \
--private-key <PK> \
--stake <amount> \
-e https://rpc.testnet.moonbeam.network
```
























