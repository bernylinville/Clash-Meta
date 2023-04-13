install

```bash
sudo useradd -r clash-meta
cd /tmp
wget https://ghproxy.com/https://github.com/MetaCubeX/Clash.Meta/releases/download/v1.14.3/clash.meta-linux-amd64-v1.14.3.gz
gzip -d clash.meta-linux-amd64-v1.14.3.gz
sudo install clash.meta-linux-amd64-v1.14.3 /usr/local/bin/Clash-Meta
sudo mkdir /etc/Clash-Meta
sudo cp config.yaml /etc/Clash-Meta
sudo cp -r yacd /etc/Clash-Meta
sudo chown -R clash-meta:clash-meta /etc/Clash-Meta
sudo cp Clash-Meta.service /etc/systemd/system
sudo systemctl daemon-reload
sudo systemctl start Clash-Meta
sudo systemctl status Clash-Meta
sudo systemctl enable Clash-Meta
```
