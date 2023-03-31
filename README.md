# Installing for Ubuntu based Linux users

### This is a step by step guide to install KDX on Linux. You'll need root access using "sudo". Follow the steps copying the commands into your console. You can use the "copy" button on each line and paste it in the shell using CTRL+SHIFT+V.

<br/>



**1. Open a shell using CTRL + ALT + T key combination**
<br/>


**2. Download package information from all configured sources**
```
sudo apt update
```
<br/>

**3. Install required packages: curl, gcc, make, git and golang**
```
sudo apt -y install curl gcc make git golang
```
<br/>

**4. Install RUST**
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh 
```
> Type 1 and press ENTER when asked
{.is-info}

<br/>

**5. Close shell**
```
exit
```
<br/>

**6. Open a new shell using CTRL + ALT + T key combination**
<br/>

**7. Install NodeJS**
```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - && sudo apt-get install -y nodejs
```
<br/>

**8. Close shell**
```
exit
```
<br/>

**9. Open a new shell using CTRL + ALT + T key combination**

<br/>

**10. Install nwjs**
```
cd ~ && mkdir bin && cd bin && wget https://dl.nwjs.io/v0.74.0/nwjs-sdk-v0.74.0-linux-x64.tar.gz && tar xvf nwjs-sdk-v0.74.0-linux-x64.tar.gz && ln -s nwjs-sdk-v0.74.0-linux-x64 nwjs && echo 'export PATH=/home/$USER/bin/nwjs:$PATH' >> ~/.bashrc
```
<br/>

**11. Close shell**
```
exit
```
<br/>

**12. Open a new shell using CTRL + ALT + T key combination**
<br/>

**13. Move to Desktop folder**
```
cd ~/Desktop/
```
<br/>

**14. Install emanator globally**
```
sudo npm install -g emanator@latest
```
<br/>

**15. Clone Aspectron's KDX github respository**
```
git clone https://github.com/aspectron/kdx.git
```
<br/>

**16. Install KDX**
```
cd kdx && npm install
```
<br/>

**17. Install kaspad binaries**
```
emanate --local-binaries
```
<br/>

**18. Run KDX**
```
nw . 
```
<br/>
<br/>

## In order to move kdx folder to another path, you need to open a shell and type:
```
mv ~/Desktop/kdx [destination path]
```

> Replace [destination path] with the path where you want to move kdx folder.
{.is-info}


For example, this will move kdx folder into your $HOME folder.
```
mv ~/Desktop/kdx ~/
```
<br/>
<br/>

## To create a shortcut on your Desktop to run KDX, open a shell and type:
```
cd ~/Desktop && echo -e '#! /bin/sh\n~/bin/nwjs/nw [path where you installed KDX]/.' >> kdx.sh && chmod +x kdx.sh
```

> Replace [path where you installed KDX] with the path where you installed KDX.
{.is-info}

For example, this will create a shortcut if you moved your kdx folder to your $HOME folder, like in the previous example:
```
cd ~/Desktop && echo -e '#! /bin/sh\n~/bin/nwjs/nw ~/kdx/.' >> kdx.sh && chmod +x kdx.sh
```
