**Table of Contents:**
- [1. Kind Installation](#1-kind-installation)
  - [1.1. Kind Design Architecture](#11-kind-design-architecture)
  - [1.2. Kind on MAC-OS](#12-kind-on-mac-os)
  - [1.3. Kind on Windows](#13-kind-on-windows)
  - [1.4. Kind on Linux](#14-kind-on-linux)
  - [1.5. Kubectl Install](#15-kubectl-install)
  - [1.6. Bash Auto Complete](#16-bash-auto-complete)
- [2. References](#2-references)


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

## 1.5. Kubectl Install

```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
   
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check   
sudo install kubectl /usr/local/bin/kubectl
kubectl version --client --output yaml

```

Ref:
- https://kubernetes.io/docs/tasks/tools/

## 1.6. Bash Auto Complete

```bash
source <(kubectl completion bash)
echo "source <(kubectl completion bash)" >> ~/.bashrc

vi /etc/bash.bashrc
alias k=kubectl
complete -o default -F __start_kubectl k

# logout and login again
```


# 2. References
- https://kind.sigs.k8s.io/docs/user/quick-start/
- https://kind.sigs.k8s.io/docs/design/initial/
- https://kubernetes.io/docs/reference/kubectl/quick-reference/