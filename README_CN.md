### This is a Chinese Translation, just because i like the MPV and Thanks for this py project !!

玩转MPV
chrome扩展和python服务器，允许你用MPV代替播放网页中的视频。
多亏了youtube-dl，它可以在数百个网站上运行，如果你安装了peerflix，它甚至可以在torrent上运行。


## 安装

安装MPV

安装python 2或3和pip

安装Chrome插件

无需使用英文说明方式安装python脚本，直接用python运行play_with_mpv.py即可

(Arch Linux）aur包可用。
 
 
## 用途

右键单击此链接并选择"播放MPV"。MPV应弹出并开始播放视频。(Ctrl+空格也行）


## 自动启动

Linux：Ubuntu为例，使rc.local可工作之后，添加一句 
nohup python /opt/play_with_mpv/play_with_mpv.py &

MacOS：暂无

Windows：

1 打开任务计划程序

2 创建基本任务

3 输入名称：playwithmpv

4 选择当用户登录时

5 选择启动程序

6 填写程序或脚本：（python.exe会前台运行，因此使用pythonw.exe后台静默运行）

C:\Users\Administrator\AppData\Local\Microsoft\WindowsApps\pythonw.exe

7 填写添加参数（可选）：（路径根据自己实际存放Python脚本的位置填写）

C:\MyApps\play-with-mpv-master\play_with_mpv.py


## MPV是高度可配置的，下面是Thann常用的配置。


从角落开始，没有边框，并保持在顶部（此点对于Windows非常重要，Win10启动程序默认不是置顶）：

*Linux*：编辑~/.配置文件/mpv/mpv.conf；*WIndows*：请根据自己安装程序的位置自行研究寻找

```yaml
ontop=yes
border=no
window-scale=0.4
geometry=100%:100%
```

要调整窗口大小而不添加边框，请添加键绑定：编辑~/.配置文件/mpv/输入. conf

```yaml
cycle border
ALT+UP add window-scale 0.05
ALT+DOWN add window-scale -0.05
```
