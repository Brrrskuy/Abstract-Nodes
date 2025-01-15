# Abstract-Nodes
Minimal spec : 32GB / 16 Core
# Update system
```
sudo apt update && sudo apt upgrade -y
```

# Install Docker + Compose (VPS New,existing Skip aja )
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y
```
# Start Docker & Enable
```
sudo systemctl start docker
```
```
sudo systemctl enable docker
```
# Clone repo
git clone https://github.com/Abstract-Foundation/abstract-node

#Go to directory
```
cd abstract-node/external-node
```
# Start node
```
docker compose --file testnet-external-node.yml up -d
```

# Check logs
```
docker logs -a 
```
```
testnet-node-external-node-1
```
```
docker logs -f --tail=0 testnet-node-external-node-1
```
# Save Pv.Key
```
cd configs
```
```
cat testnet_consensus_secrets.yaml
```
