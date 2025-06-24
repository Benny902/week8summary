
---

## Deployment Entry - 2025-06-24 14:30:18

**Public IP:** null  
**Region:** eastus2  
**VM Size:** Standard_B1ls  
**Image:** 0001-com-ubuntu-server-jammy 22_04-lts-gen2

### Azure CLI Commands Used
- az login --use-device-code
- az group create --name bennyVMeastus2 --location eastus2
- az vm create --resource-group bennyVMeastus2 --name myvm --image 0001-com-ubuntu-server-jammy 22_04-lts-gen2 --size Standard_B1ls ...
- az network public-ip update --allocation-method Static
- az vm open-port --port 22 ...
- scp ./ to VM
- docker-compose up -d

### Deployment Method
- GitHub Actions CI/CD (via deploy-vm.yml)

### Healthcheck
- curl http://null:3000

### Reboot Test
- App recovered after reboot

### Browser Compatibility
- Chrome
- Firefox
- Mobile
