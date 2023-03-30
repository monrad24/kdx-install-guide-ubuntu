
# KDX install guide for Ubuntu based Linux

Small step-by-step guide to install KDX on Linux


1. Open the shell using CTRL + ALT + T key combination

---

2. Download package information from all configured sources
```
sudo apt update
```

---

3. Install requirements: curl, gcc, make, git and golang
```
sudo apt -y install curl gcc make git golang
```

---

4. Install RUST
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh 
```
Press 1 and ENTER when asked

---

5. Close shell
```
exit
```

---

6. Open a new shell using CTRL + ALT + T key combination

---

7. Install NodeJS
```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - && sudo apt-get install -y nodejs
```

---

8. Close shell
```
exit
```

---

9. Open a new shell using CTRL + ALT + T key combination

---

10. Install nwjs
```
cd ~ && mkdir bin && cd bin && wget https://dl.nwjs.io/v0.74.0/nwjs-sdk-v0.74.0-linux-x64.tar.gz && tar xvf nwjs-sdk-v0.74.0-linux-x64.tar.gz && ln -s nwjs-sdk-v0.74.0-linux-x64 nwjs && echo 'export PATH=/home/$USER/bin/nwjs:$PATH' >> ~/.bashrc
```

---

11. Close shell
```
exit
```

---

12. Open a new shell using CTRL + ALT + T key combination

---

13. Create KDX folder on Desktop (it can be moved later)
```
cd ~/Desktop/ && mkdir kdx && cd kdx
```

---

14. Install emanator globally
```
sudo npm install -g emanator@latest
```

---

15. Clone Aspectron's KDX github respository
```
git clone https://github.com/aspectron/kdx.git
```

---

16. Install KDX
```
cd kdx && npm install
```

17. Install kaspad binaries
```
emanate --local-binaries
```

---

18. Run KDX
```
nw . 
```
