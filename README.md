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
**avalanche**











