# Install-Linux-Mint-WARP
It's a "How to install WARP at Linux Mint" guide.


## 1 - Add cloudflare gpg key.
```
curl -fsSL https://pkg.cloudflareclient.com/pubkey.gpg | sudo gpg --yes --dearmor --output /usr/share/keyrings/cloudflare-warp-archive-keyring.gpg
```



## 2 - Find your Mint's "PACKAGE BASE".

https://linuxmint.com/download_all.php

For example. I am using Xia and Xia = noble


![example](https://github.com/user-attachments/assets/512ab778-5c09-48fe-a62a-69224edd4b4c)




## 3 - Add this repo to your apt repositories.

For Xia 22.1 (noble):
```
echo "deb [arch=amd64, signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ noble main" | sudo tee /etc/apt/sources.list.d/cloudflare-client.list
```

For others:

(change YOUR_PACKAGE_BASE to your package base)
```
echo "deb [arch=amd64, signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ YOUR_PACKAGE_BASE main" | sudo tee /etc/apt/sources.list.d/cloudflare-client.list
```



## 4 - Install.
```
sudo apt-get update && sudo apt-get install cloudflare-warp
```
