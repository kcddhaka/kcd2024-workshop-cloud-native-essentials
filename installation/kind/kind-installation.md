**Table of Contents:**
- [1. Kind Installation](#1-kind-installation)
  - [1.1. Kind Design Architecture](#11-kind-design-architecture)
  - [1.2. Kind on MAC-OS](#12-kind-on-mac-os)
  - [1.3. Kind on Windows](#13-kind-on-windows)
  - [1.4. Kind on Linux](#14-kind-on-linux)
- [2. Bash Auto Complete](#2-bash-auto-complete)
- [3. logout and login again](#3-logout-and-login-again)
- [4. References](#4-references)


# 1. Kind Installation


## 1.1. Kind Design Architecture 
![Kind](https://kind.sigs.k8s.io/docs/images/diagram.png)


## 1.2. Kind on MAC-OS

On macOS via Homebrew:
```bash
brew install kind
```

## 1.3. Kind on Windows
On Windows via Chocolatey (https://chocolatey.org/packages/kind):
```bash
choco install kind
```

On Windows in PowerShell:
```bash
# download kind binary
curl.exe -Lo kind-windows-amd64.exe https://kind.sigs.k8s.io/dl/v0.22.0/kind-windows-amd64
# Move-Item .\kind-windows-amd64.exe c:\some-dir-in-your-PATH\kind.exe


# move file
New-Item -Path "c:\" -Name "kind" -ItemType "directory"
Move-Item .\kind-windows-amd64.exe c:\kind\kind.exe


# set env manually so that kind.exe is avilable in command line
# setx /m PATH "%PATH%;c:\kind\"
# echo %PATH%
# setx PATH "$env:path;c:\kind\" -m
```


## 1.4. Kind on Linux
```bash
# For AMD64 / x86_64
[ $(uname -m) = x86_64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.22.0/kind-linux-amd64
# For ARM64
[ $(uname -m) = aarch64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.22.0/kind-linux-arm64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/kind
```



# 2. Bash Auto Complete

```bash
source <(kubectl completion bash)
echo "source <(kubectl completion bash)" >> ~/.bashrc

vi /etc/bash.bashrc
alias k=kubectl
complete -o default -F __start_kubectl k

# 3. logout and login again
```- [Kind Installation](#kind-installation)
  - [Kind Design Architecture](#kind-design-architecture)
  - [Kind on MAC-OS](#kind-on-mac-os)
  - [Kind on Windows](#kind-on-windows)
  - [Kind on Linux](#kind-on-linux)
- [5. Bash Auto Complete](#5-bash-auto-complete)
- [References](#references)




# 4. References
- https://kind.sigs.k8s.io/docs/user/quick-start/
- https://kind.sigs.k8s.io/docs/design/initial/