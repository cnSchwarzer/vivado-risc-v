[Original Readme](README.original.rst)

# vivado-risc-v for REITO

Add REITO support in vivado-risc-v
 
## Suggestions

Use [tio](https://github.com/tio/tio) to connect to the board via USB serial, it supports control characters and colors.

Mirror `apt` 
```
deb [arch=riscv64] http://mirror.sjtu.edu.cn/debian-ports unstable main
deb [arch=riscv64] http://mirror.sjtu.edu.cn/debian-ports unreleased main
```

``` 
sudo apt -y --allow-unauthenticated --allow-insecure-repositories -o "Acquire::https::Verify-Peer=false" update 
sudo apt -y --allow-unauthenticated -o "Acquire::https::Verify-Peer=false" install ca-certificates gnupg
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8D69674688B6CB36  
sudo apt-key export 8D69674688B6CB36 | sudo gpg --dearmour -o /etc/apt/trusted.gpg.d/apt.gpg
sudo apt update
```

```
sudo gpg --keyserver keyserver.ubuntu.com --recv-keys 8D69674688B6CB36 
sudo gpg -a --export 8D69674688B6CB36 | sudo apt-key add -
```