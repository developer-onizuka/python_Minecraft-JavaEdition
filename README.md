# python_Minecraft-JavaEdition


Use the virt-io driver instead of VGA and check 3D accelation for for accepting OpenGL command at Virtual Machine.

```
$ sudo visudo
$ sudo apt-get install -y curl
$ sudo apt-get install -y wget
$ wget https://launcher.mojang.com/download/Minecraft.deb
$ sudo dpkg -i Minecraft.deb 

$ sudo apt-get install -y default-jre
$ sudo apt --fix-broken install
$ sudo apt-get install -y openjdk-8-jre
$ echo 2| sudo update-alternatives --config java

$ sudo dpkg -i Minecraft.deb 

start minecraft

$ wget https://maven.minecraftforge.net/net/minecraftforge/forge/1.12.2-14.23.5.2855/forge-1.12.2-14.23.5.2855-installer.jar
$ java -jar forge-1.12.2-14.23.5.2855-installer.jar 

$ wget https://github.com/arpruss/raspberryjammod/releases/download/0.94/mods.zip
$ unzip mods.zip
$ cd 1.12.2/
$ cp -p RaspberryJamMod.jar ~/Desktop/Forged1.12.2/mods/
$ sudo apt-get update
$ sudo apt-get install python3-pip
$ pip3 install mcpi
   
$ cat<<EOF > hello-world.py 
from mcpi import minecraft
mc = minecraft.Minecraft.create()
mc.postToChat('Hello World!')
EOF

$ python3 hello-world.py 
```
