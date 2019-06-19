# 利用Capslock
## Linux下快捷键解决方案
在windows上，有AHK这种大杀器，可以将Capslock键设置为一个辅助按键。奈何换到Ubuntu不能用AHK。网上有人说可以用wine运行AHK，但总觉得太过麻烦。

于是google一番，设置好了在Ubuntu下的按键映射。

- 下载Autokey：https://github.com/autokey/autokey
- 将Capslock映射为Hyper，终端输入：  
```sh
setxkbmap -option caps:hyper 
```
- Autokey有用户界面，摸索着设置就可以，将辅助按键多设置为Hyper（因为上面把Capslock映射为Hyper了），这样就在Ubuntu上将Capslock利用了起来。要注意的是如果发送多个键要用  send_keys(...)

- Autokey的部分配置文件放在本仓库。在本地的存储位置为：  /home/[your_name]/.config/autokey/data

有些linux发行版可能会有一些系统快捷键，主要涉及到的是L键，例如锁屏等。可通过系统设置将快捷键修改，或者修改autokey中的快捷键也可以。
另外如果没有系统设置快捷键，可以安装dconf-editor，不过这个修改很危险，可能造成系统崩溃，要慎重。

部分常用的按键映射如下（以实际效果为准，Autokey中还要映射）：
```
Capslock + j ---> left
Capslock + l ---> right
Capslock + i ---> up
Capslock + k ---> down
Capslock + u ---> home
Capslock + o ---> end
Capslock + Shift + j ---> Shift + left
Capslock + Shift + l ---> Shift + right
Capslock + Shift + i ---> Shift + up
Capslock + Shift + k ---> Shift + down
Capslock + Shift + u ---> Shift + home
Capslock + Shift + o ---> Shift + end
Capslock + Ctrl + j ---> Ctrl + left
Capslock + Ctrl + l ---> Ctrl + right
Capslock + Ctrl + i ---> Ctrl + up
Capslock + Ctrl + k ---> Ctrl + down
Capslock + s ---> Ctrl + s
```

## Windows下解决方案

- 下载AHK，安装。
- 脚本CapsLock.ahk实现了上述基本映射功能。该脚本是网上找来的，做了一点修改，如果已安装AHK的话下载下来双击即可运行。
