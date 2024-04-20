

Docker is a powerful platform for developing, shipping, and running applications inside containers. This guide will walk you through the steps of installing Docker on Windows, macOS, and Linux.

## Table of Contents
- [Windows](#Windows)
- [macOS](#macOS)
- [Linux](#Linux)

## Windows
### Step 1: System Requirements
Ensure your system meets the requirements for Docker Desktop on Windows:
- Windows 10 64-bit: Pro, Enterprise, or Education (Build 16299 or later).
- Hyper-V and Containers Windows features must be enabled.

### Step 2: Download Docker Desktop
1. Go to [Docker Hub](https://hub.docker.com/editions/community/docker-ce-desktop-windows/).
2. Click on "Get Docker" to download the installer.

### Step 3: Install Docker Desktop
1. Run the downloaded Docker Desktop Installer.
2. Follow the on-screen instructions to complete the installation.

### Step 4: Start Docker Desktop
- Docker will start automatically after installation. You can also start it from the Start menu.

### Step 5: Verify Installation
- Open a command prompt and type `docker --version` to check the Docker version.

## macOS
### Step 1: System Requirements
Ensure your macOS meets the following requirements:
- Mac hardware must be a 2010 or newer model.
- macOS must be version 10.14 or newer.
- At least 4 GB of RAM.

### Step 2: Download Docker Desktop
1. Go to [Docker Hub](https://hub.docker.com/editions/community/docker-ce-desktop-mac/).
2. Click on "Get Docker" to download the Docker Desktop for Mac.

### Step 3: Install Docker Desktop
1. Open the downloaded `.dmg` file.
2. Drag and drop Docker into your Applications folder.

### Step 4: Start Docker Desktop
- Open Docker from your Applications folder.

### Step 5: Verify Installation
- Open a terminal and type `docker --version` to confirm Docker is correctly installed.

## Linux
### Step 1: Set Up the Repository
1. Update your package index: `sudo apt-get update`.
2. Install packages to allow apt to use a repository over HTTPS:
   ```bash
   sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
3. Add Docker’s official GPG key:
`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`

### Step 2: Install Docker Engine

1. Set up the stable repository:
    
    bashCopy code
    
    `echo \ "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`
    
2. Update the apt package index:
    
    bashCopy code
    
    `sudo apt-get update`
    
3. Install the latest version of Docker Engine and containerd:
    
    bashCopy code
    
    `sudo apt-get install docker-ce docker-ce-cli containerd.io`

### Step 3: Start Docker

- Start the Docker service: `sudo systemctl start docker`.

### Step 4: Verify Installation

- Run `docker --version` to ensure Docker is installed correctly.