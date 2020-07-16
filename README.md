# scrcpy手机投屏教程
***
> 一款高分辨率，高帧率，低延迟，跨平台的开源安卓手机投屏神器  

## 1. 用途
- 部分代替handoff、airdrop、sidecar、airplay
- 高清直播、演示、讲课、分享、录屏

## 2. 安装
```zsh
#mbp安装adb 
brew cask install android-platform-tools
#查看设备ID
adb devices
#mbp安装scrcpy
brew install scrcpy
```

## 3. 使用
> 小米8 MIUI11投屏MacBook Pro2018 macOS Catalina

- 开启电源，打开外接显示器*LG 27UL850*
- 打开外接键盘*iKBC W200*&鼠标*Lofree Maus*，任意操作唤醒mbp
- 输入*~~password~~*解锁mbp
- 手机开启调试方法：“设置”->“我的设备”->“全部参数”->点击7下MIUI版本，开启“开发者选项”，重新进入 “设置”->“更多设置”->“开发者选项” 中同时开启 USB调试 和 USB调试(安全设置)。
- 连接手机
- `command+u`打开终端
- 终端内输入`scrcpy`，按下**Enter**运行
- `command+f`全屏*&*退出全屏
- 关闭投屏&鼠标
- `command+control+p`休眠mbp
- 关闭显示器&键盘
- 关闭电源 

## 4. 常用命令
功能 | 参数&快捷键
-- | --
关闭手机屏幕 | scrcpy -S
限制画面分辨率 | scrcpy -m 1024 (比如限制为 1024)
修改视频码率 | scrcpy -b 4M (默认 8Mbps，改成 4Mbps)
裁剪画面 | scrcpy -c 1224:1440:0:0<br/>表示分辨率1224x1440 并且偏移坐标为 (0,0)
多设备切换 | scrcpy -s 设备ID (使用 adb devices 命令查看设备ID)
窗口置顶 | scrcpy -T
显示触摸点击 | scrcpy -t<br/>在演示或录制教程时，可在画面上对应显示出点击动作
全屏显示 | scrcpy -f
文件传输默认路径 | scrcpy --push-target /你的/目录<br/>将文件拖放到 | scrcpy可以传输文件，此命令指定默认保存目录
只读模式(仅显示不控制) | scrcpy -n
屏幕录像 | scrcpy -r 视频文件名.mp4 或 .mkv
屏幕录像 (禁用电脑显示) | scrcpy -Nr 文件名.mkv
设置窗口标题 | scrcpy --window-title '异次元好棒！'
切换全屏模式 | Control+F
将窗口调整为1：1（完美像素） | Control+G
调整窗口大小以删除黑色边框 | Control+X | 双击黑色背景
设备HOME键 | Control+H | 鼠标中键
设备BACK键 | Control+B | 鼠标右键
设备任务管理 键 (切换APP) | Control+S
设备菜单键 | Control+M
设备音量+键 | Control+↑
设备音量-键 | Control+↓
设备电源键 | Control+P
点亮手机屏幕 | 鼠标右键
复制内容到设备 | Control+V
启用/禁用 FPS 计数器（stdout） | Control+i

## 5. 参考
- [1] [Scrcpy - 开源免费在电脑显示手机画面并控制手机的工具 (投屏/录屏/免Root)](https://www.iplaysoft.com/scrcpy.html) 
- [2] [scrcpy——Android投屏神器(使用教程)](https://blog.csdn.net/was172/article/details/99705855) 
- [3] [如何将android手机屏幕投影至Mac](https://www.zhihu.com/question/38722634/answer/1169220702) 

<br/>

***
&copy;2020/7/13 Chen Yuxin. All rights reserved# scrcpy手机投屏教程
***
