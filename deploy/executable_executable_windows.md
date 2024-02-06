# 使用windows部署面板
## 1.准备需要的文件
### 1.1.下载
- 下载页面地址: [https://github.com/zaigie/palworld-server-tool/releases/latest](https://github.com/zaigie/palworld-server-tool/releases/latest)
- 请下载`pst_**_windows_x86_64.zip`文件
- 将文件提取到一个空文件夹中(注意文件夹的路径不应该有中文和空格)
  - 如`C:\\palworld\\pst`是推荐路径
- 记住该路径,下面修改`config.yaml`中需要修改`save.decode_path`的值为`该路径\\sav_cli.exe`

## 2.修改配置文件`config.yaml`
**请认真仔细阅读下方的[配置获取方式说明](#配置获取方式说明)**
> 注意配置文件的编码格式要求是`ANSI`

```yaml
web: # web 相关配置
  password: "" # web 管理模式密码
  port: 8080 # web 服务端口
  tls: false # 是否开启 TLS
  cert_path: "" # Cert 文件路径,如果不开启tls,则不需要配置
  key_path: "" # Key 文件路径,如果不开启tls,则不需要配置
rcon: # RCON 相关配置
  address: "127.0.0.1:25575" # RCON 地址
  password: "" # 设置的 AdminPassword
  timeout: 5 # 请求 RCON 超时时间，推荐 <= 5
  sync_interval: 60 # 定时向 RCON 服务获取玩家在线情况的间隔，单位秒
save: # 存档文件解析相关配置
  path: "/path/to/your/Pal/Saved" # 存档文件路径
  decode_path: "/path/to/your/sav_cli" # 存档解析工具路径
  sync_interval: 120 # 定时从存档获取数据的间隔，单位秒，推荐 >= 120
manage: # 管理相关
  kick_non_whitelist: false # 玩家不在白名单是否自动踢出
```
- **确保`rcon`的配置项修改正确**
- **确保`save`的配置修改正确**

### 1.1.配置获取方式说明
- [rcon配置](../qa/rcon.md)
- [save配置](../qa/save.md)
  - `decode_path`的值,是压缩包解压后所在路径中`sav_cli.exe`文件的路径
  - 请查看其中的**windows**章节
## 3.运行

## 4.如何确认程序是否正常运行
- [程序运行说明](../qa/pts.md)
