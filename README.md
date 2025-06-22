# 🐳 How to Install Docker on Ubuntu

This guide walks you through installing Docker Engine on Ubuntu (20.04 / 24.04).  
Tested and verified as of 2025.

---

## 📦 1. Update the Package Index
```bash
sudo apt update
```

## 📥 2. Install Required Dependencies
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
```

## 🔐 3. Add Docker’s Official GPG Key
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

## 📚 4. Add Docker’s APT Repository
```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

## 🔍 5. Verify Docker Repository is Added
```bash
apt-cache policy docker-ce
```

## 🐳 6. Install Docker Engine
```bash
sudo apt install docker-ce -y
```

## ✅ 7. Check Docker Service Status
```bash
sudo systemctl status docker
```

## 🚀 Test Docker Installation (Optional)
```bash
sudo docker run hello-world
```
This command runs a test image to confirm Docker is working properly.

## 📌 Notes
Docker must be run with sudo by default. To run without sudo, add your user to the docker group:
```bash
sudo usermod -aG docker $USER
```

# Happy containerizing!