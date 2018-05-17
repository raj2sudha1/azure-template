# azure-template
azure template to create windowsserver 2016


# docker-windows-azure

## Windows Server 2016 LTS channel

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%raj2sudha1%2Fazure-template%2Fmaster%2Ftemplate.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>


Login into Azure Vm and install git
```bash
$ choco install git -params '"/GitAndUnixToolsOnPath /WindowsTerminal"' -y
```
### Test drive

Just run it in a clean environment creating two folders on your host:

```powershell
mkdir server
mkdir client\.docker
docker run --rm `
  -e SERVER_NAME=$(hostname) `
  -e IP_ADDRESSES=127.0.0.1,192.168.254.135 `
  -v "$(pwd)\server:c:\programdata\docker" `
  -v "$(pwd)\client\.docker:c:\users\containeradministrator\.docker" raj2sudha/dockertls-windows-1709
dir server\certs.d
dir server\config
dir client\.docker
```

