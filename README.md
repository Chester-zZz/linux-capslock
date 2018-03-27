# Linux下快捷键解决方案
在windows上，有AHK这种大杀器，可以将Capslock键设置为一个辅助按键。奈何换到Ubuntu不能用AHK。网上有人说可以用wine运行AHK，但总觉得太过麻烦。

于是google一番，设置好了在Ubuntu下的按键映射。

- 下载Autokey：https://github.com/autokey/autokey
- 将Capslock映射为Hyper，终端输入：  
```sh
setxkbmap -option caps:hyper 
```
- Autokey有用户界面，摸索着设置就可以，将辅助按键多设置为Hyper（因为上面把Capslock映射为Hyper了），这样就在Ubuntu上将Capslock利用了起来。要注意的是如果发送多个键要用  send_keys(...)

- Autokey的部分配置文件放在本仓库。在本地的存储位置为：  /home/[your_name]/.config/autokey/data
