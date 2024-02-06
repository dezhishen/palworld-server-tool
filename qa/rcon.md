# RCON相关说明
## 如何开启私服 RCON
需要开启服务器的 RCON 功能，如果你的私服教程有写更好，没有的话，修改 PalWorldSettings.ini 文件
**也就是修改游戏内各种倍数、概率的那个文件，里面最后的位置有如下：**
```
AdminPassword=...,...,RCONEnabled=true,RCONPort=25575
```
- RCONEnabled=true,代表开启
- AdminPassword是密码,可以为空(**如果你的服务器25575端口外网可以访问,请务必设置密码**)
- RCONPort=25575表示你端口为25575