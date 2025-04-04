# 🗓️ Meeting Agenda: Azure Resource Testing & Connectivity Setup

Objective: Validate connectivity and verify setup for Azure-hosted components (Databases).

## Azure Resource Testing
1. Way to connect **platform20maindb** using pgadmin
- prerequisite : pgadmin4
```sh
General
Name : platform20maindb
Connection
Host: CONFIDENTIAL
Port: 5432
MaintainceDatabase: CONFIDENTIAL
Username: adminUser
Password: CONFIDENTIAL
```
2. Way to connect **platform20orgdb** using pgadmin
- prerequisite : pgadmin4
```sh
General 
Name : platform20orgdb
Connection
Host: CONFIDENTIAL
Port: 5432
MaintainceDatabase: CONFIDENTIAL
Password: CONFIDENTIAL
```

---
## Steps to Install PGADMIN4 on Windows/macOS
### Download Desktop Version (Windows/macOS)
1. Visit https://www.pgadmin.org/download/
2. Download the appropriate installer for your OS
3. Run the installer and follow the prompts
### Connecting to PostgreSQL Database
- Launch pgAdmin4 (either via web interface or desktop app)
- Right-click "Servers" and select "Create" > "Server"
- In the "General" tab, enter a name for your connection
- In the "Connection" tab:
    - Host: localhost (or your server IP)
    - Port: 5432 (default PostgreSQL port)
    - Maintenance database: postgres
    - Username: Your PostgreSQL username
    - Password: Your PostgreSQL password
- Click "Save" to establish the connection
---
## Steps to instal azure cli
### Install Azure CLI on Windows
#### Install via MSI (Recommended)
1. Download the latest Azure CLI MSI installer:
   👉 [Azure CLI for Windows (64-bit)](https://aka.ms/installazurecliwindows)
2. Run the downloaded `.msi` file.
3. Follow the installation wizard.
4. Open **Command Prompt** or **PowerShell** and verify installation:

```bash
   az version
```
## Install Azure CLI on macOS
###  Install via Homebrew (Recommended)
#### Install Homebrew (if not already installed):
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
-Install Azure CLI: 
```sh
brew update && brew install azure-cli
az --version
```

