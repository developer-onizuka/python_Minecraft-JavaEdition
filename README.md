# python_Minecraft-JavaEdition


Use the virt-io driver instead of VGA and check 3D accelation for for accepting OpenGL command at Virtual Machine.

```
$ sudo visudo
$ sudo apt-get install -y curl
$ sudo apt-get install -y wget
$ wget https://launcher.mojang.com/download/Minecraft.deb
$ sudo dpkg -i Minecraft.deb 

$ sudo apt-get install -y default-jre
$ sudo apt-get install -y default-jre-headless
$ sudo apt --fix-broken install
$ sudo apt-get install -y default-jre

$ sudo dpkg -i Minecraft.deb 
$ sudo apt -y install openjdk-8-jre
$ sudo update-alternatives --config java

$ java -jar forge-1.12.2-14.23.5.2855-installer.jar 


$ cd ../Downloads/mods/1.12.2/
$ cp -p RaspberryJamMod.jar ~/Desktop/Forged1.12.2/mods/
$ sudo apt-get update
$ sudo apt-get install python3-pip
$ pip3 install mcpi-e
   
$ cat<<EOF > hello-world.py 
from mcpi_e import minecraft
mc = minecraft.Minecraft.create()
mc.postToChat('Hello World!')
EOF

$ python3 hello-world.py 
```
