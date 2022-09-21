# telegram_channel_downloader
Telegram 频道/群组 文件下载脚本

脚本需要python3环境，具体安装教程自行搜索。

centos7需要更新openssl，且python版本不能是3.10.x，只能安装3.9.x版本的。


**1. 前提**
 
 - 更新openssl
 
   必须要安装1.1.1版本以上的，安装教程自行百度

 - 安装python3.9.14
   
   需要编译安装，ssl使用上面安装的版本
 
 
 - 从 https://my.telegram.org/apps 获取自己的Telegram API密钥。

 - 下载脚本
 ```
 git clone https://github.com/bluesky4485/telegram_channel_downloader_py39.git
 ```

**2. 使用**

 - 进入脚本目录
 ```
 cd telegram_channel_downloader
 ```
 - 安装依赖 
 
 ```
 pip3 install -r requirements.txt
 ```

 - 修改telegram_channel_downloader.py文件内的 api_id 和 api_hash 为你自己的

 - 修改脚本内的频道名称、保存路径、 bot_token 、 admin_id 、 chat 等必填配置
 
 - 鉴于网友需要上传GD，特添加了使用clone自动上传到团队盘的功能，需要在配置区域设置。具体查看脚本内注释

 - rclone安装自行百度，安装后配置好对应的网盘，需要将代码中网盘配置部分按照配置情况进行修改
   
 - 运行  
 ```
 python3 tg_channel_downloader.py
 ```
 - 按照提示输入telegram绑定的手机号获取验证码并输入
 
 - 配置完成后需要给bot发送 /start 频道的链接 0 才会正式开始运行脚本，否则无法启动 0代表开始下载消息的ID，可以自行修改。
 