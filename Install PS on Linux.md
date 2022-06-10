# Install PS on Linux

>https://docs.microsoft.com/en-us/powershell/scripting/install/install-debian?view=powershell-7.2
## Installing PowerShell on Debian Linux
>PowerShell 7.2.4 
```
https://github.com/PowerShell/PowerShell/releases/download/v7.2.4/powershell-lts_7.2.4-1.deb_amd64.deb
```
>PowerShell 7.0.10
```
Debian 10 - https://github.com/PowerShell/PowerShell/releases/download/v7.0.10/powershell-lts_7.0.10-1.debian.10_amd64.deb
```
```
Debian 9 - https://github.com/PowerShell/PowerShell/releases/download/v7.0.10/powershell-lts_7.0.10-1.debian.9_amd64.deb
```
## Installation on Debian 11 via Package Repository
// Install system components
```
sudo apt update  && sudo apt install -y curl gnupg apt-transport-https
```

// Import the public repository GPG keys
```
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
```

// Register the Microsoft Product feed
```
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-debian-bullseye-prod bullseye main" > /etc/apt/sources.list.d/microsoft.list'
```

// Install PowerShell
```
sudo apt update && sudo apt install -y powershell
```

// Start PowerShell
```
pwsh
```

## Installation on Debian 10 via Package Repository
// Download the Microsoft repository GPG keys
```
wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb
```

// Register the Microsoft repository GPG keys
```
sudo dpkg -i packages-microsoft-prod.deb
```

// Update the list of products
```
sudo apt-get update
```

// Install PowerShell
```
sudo apt-get install -y powershell
```

// Start PowerShell
```
pwsh
```
## Uninstallation
```
sudo apt-get remove powershell
```