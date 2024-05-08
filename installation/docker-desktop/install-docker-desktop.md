**Table of Contents:**
- [1. Install Docker Desktop](#1-install-docker-desktop)
  - [1.1. Docker Desktop for Windows](#11-docker-desktop-for-windows)
  - [1.2. Docker Desktop for Linux](#12-docker-desktop-for-linux)
  - [1.3. Docker Desktop for Mac](#13-docker-desktop-for-mac)
- [2. References](#2-references)
- [3. Appendix](#3-appendix)


# 1. Install Docker Desktop

## 1.1. Docker Desktop for Windows 

Kind can run using Windows Subsystem for Linux 2 (WSL2) on Windows 10 onwards. [Details procedure can be found here](https://kind.sigs.k8s.io/docs/user/using-wsl2/). However, docker desktop installer will install WSL2 as part of following procedure. 


Follow below steps to complete the docker desktop installation: 
- [Download docker desktop binary file](https://docs.docker.com/desktop/install/windows-install/)
- Double click on the downloaed binary installer
- Click "Yes" button
- In the next screen, please tick mark following options:  
  - Use WSL2
  - Add shortcut to desktop
- Installation process will begin by unpacking the installer binary file
- Logout windows to complete the installation > signout anyway if prompted
- Login again to windows and accept subscription service agreement 
- Skip survey button (based on your preference)


## 1.2. Docker Desktop for Linux

[Follow me to install docker on linux platform](https://docs.docker.com/desktop/install/linux-install/).


## 1.3. Docker Desktop for Mac
[Follow me to install docker on Mac](https://docs.docker.com/desktop/install/mac-install/)




# 2. References
- https://docs.docker.com/get-docker/
- https://docs.docker.com/desktop/install/windows-install/
- https://docs.docker.com/desktop/wsl/
- https://kind.sigs.k8s.io/docs/user/using-wsl2/
- https://docs.docker.com/desktop/install/linux-install/
- https://docs.docker.com/desktop/install/mac-install/


# 3. Appendix