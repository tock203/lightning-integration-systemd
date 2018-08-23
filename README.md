# lightning-integration-systemd
A systemd service/timer to run [lightning-integration](https://github.com/cdecker/lightning-integration) periodically

## Installation
```
sudo -H az login

git clone https://github.com/tock203/lightning-integration-systemd.git /opt/lightning-integration-systemd -b until-dockerfile-merged
cd /opt/lightning-integration-systemd
# Edit AZURE_STORAGE_ACCOUNT in lightning-integration.service according to your environment

sudo cp lightning-integration.service lightning-integration.timer /etc/systemd/system/
systemctl daemon-reload
systemctl enable --now lightning-integration.timer
```

## Requirements
- Docker
- Git
- Azure CLI >= 2.0
