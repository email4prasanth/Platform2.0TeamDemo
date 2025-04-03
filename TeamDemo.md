
# Azure Resource Testing
1. Static web app URL - https://icy-river-00d5a6d0f.6.azurestaticapps.net
2. Way to connect **platform20maindb** using pgadmin
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
3. Way to connect **platform20orgdb** using pgadmin
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
4. Ways to connect **VM** using putty
- prerequisite: Putty, platform20_private.ppk
```
- Install putty 
- Under saved session type platform20_etl
- click on platform20_etl 
- Left side Connections >> SSH >> Auth >> Credentials >> public key for authentication Browse the key platform20_private.ppk file
- Go to session click on platform20_etl and save
- Paste <PublicIp> in the hostname make sure port is 22
- Now enter adminuser
- If you want to increase the font size go to top white border right click change settings >> platform20_etl >>Apperance >> Font Bold 18 >> Apply >>OK.
```
- Manual Verification Steps
```sh
# Verify Docker installation
docker --version
docker compose version
systemctl status docker

# Verify Node.js installation
node --version
npm --version

# Verify Python installation
python3 --version
pip3 --version
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

## Steps to Install PuTTY on Windows/macOS
### For Windows:
#### Method 1: Official Installer  
1. Go to the official PuTTY download page:  
   [PuTTY Download Page](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)  
2. Under **"Package files"**, look for:  
   - `putty-64bit-X.XX-installer.msi` (for 64-bit Windows)  
   - `putty-X.XX-installer.msi` (for 32-bit Windows)  
3. Click the MSI installer link to download.  
4. Run the downloaded `.msi` file.  
5. Follow the installation wizard (you can accept all defaults).  
6. PuTTY will be installed in your **Start Menu**.  

#### Verifying the Installation (Windows):  
1. Open **Start Menu** and search for **"PuTTY"**.  
2. Click to launch the application.  

---

### For macOS:
#### Method 1: Using Homebrew  
1. Open **Terminal**.  
2. Install Homebrew (if not installed):  
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
3. Install PuTTY: `brew install putty`.
### Method 2: Using MacPorts  
1. Install MacPorts (if not installed):  
   [MacPorts Installation](https://www.macports.org/install.php)  
2. Open **Terminal** and run:  
   ```bash
   sudo port install putty
#### Verifying the Installation (macOS):
- Open Terminal and type: `putty`
