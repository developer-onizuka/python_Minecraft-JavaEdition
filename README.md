# python_Minecraft-JavaEdition


Use the virt-io driver instead of VGA and check 3D accelation for for accepting OpenGL command at Virtual Machine.

# 1. Install Ubuntu on Virtual Machine using KVM or Virtualbox

# 2. visudo for no password required
After edit below, you can quit with Cntrl+X. But don't forget saving.
```
$ sudo visudo
<your name> ALL=NOPASSWD: ALL
```

# 3. Install JRE and Minecraft Java-Edition(Demo-Edition)
```
$ sudo apt-get install -y wget
$ wget https://launcher.mojang.com/download/Minecraft.deb
$ sudo apt-get install -y default-jre
$ sudo apt-get install -y openjdk-8-jre
$ echo 2 | sudo update-alternatives --config java
$ sudo dpkg -i Minecraft.deb 
```

# 4. Once Launch Minecraft thru icon click of Minecraft

# 5. Install Minecraft Forge
```
$ wget https://maven.minecraftforge.net/net/minecraftforge/forge/1.12.2-14.23.5.2855/forge-1.12.2-14.23.5.2855-installer.jar
$ java -jar forge-1.12.2-14.23.5.2855-installer.jar 
```

# 6. Select Installations tab on the Minecraft Launcher's GUI

# 7. Edit Installation of forge-1.12.2 and Edit Game Directly like "/home/xxx/Desktop/Forged1.12.2" 

# 8. Download Mod and copy it Game Directly you created at #7's step
```
$ wget https://github.com/arpruss/raspberryjammod/releases/download/0.94/mods.zip
$ unzip mods.zip
$ cd 1.12.2/
$ cp -p RaspberryJamMod.jar ~/Desktop/Forged1.12.2/mods/
```

# 9. Restart Minecraft and Check the mod is available
It is succeed if you can find "Raspberry Jam Mod 0.92" in the window of Mod list.

# 10. Install pip3 and mcpi which is the library to operate Minecraft with python 
```
$ sudo apt-get update
$ sudo apt install openssh-server
$ sudo apt-get install python3-pip
$ pip3 install mcpi
```

# 11. Hello world on Minecraft
```
$ cat<<EOF > hello-world.py 
from mcpi import minecraft
mc = minecraft.Minecraft.create()
mc.postToChat('Hello World!')
EOF

$ python3 hello-world.py 
```

# 12. (Optional) Setting SSH environment
```
$ sudo virsh domifaddr minecraft
 Name       MAC address          Protocol     Address
-------------------------------------------------------------------------------
 vnet0      52:54:00:c3:67:15    ipv4         192.168.122.162/24

$ cd
$ ssh-keygen -t rsa -N '' -f ~/.ssh/id_rsa <<< y
$ ssh-copy-id -i ~/.ssh/id_rsa.pub <username>@192.168.122.162
```
