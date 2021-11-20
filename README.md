# kyve
Preparing to install
Open metamask and add **Moonbase Alpha**
add token KYVE. Contract: 0xb5e10F806e86b7d2415c126d8864032f12325BBE
open https://app.kyve.network/faucet
Click on share on twitter
Add you link with share twitter and click ''Claim your tokens''

# install
sudo apt-get update && sudo apt-get upgrade -y
```
docker install (one command)
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
