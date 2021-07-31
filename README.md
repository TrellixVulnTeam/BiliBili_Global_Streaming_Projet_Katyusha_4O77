# BiliBili_Global_Streaming_Project_Katyusha
尝试解决海外主播无法在哔哩哔哩直播的“系统升级中”问题  
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
尝试解决海外主播无法在批哩批哩直播的问题  
“Remove ChenRui Resistance Stronk”  
  
原理：批哩批哩封锁海外IP直播，本项目尝试使主播向YouTube推流，使用YouTube作为跳板，同时肉身在墙内的转播MAN接收主播在YouTube（需要翻墙）的直播，使用墙内IP转播推流到批哩批哩

优点: 不需要公网IP，可以在粉丝的个人电脑上运行
     不需要对视频解码编码，可以在配置低下的PC上运行
     比使用回国VPN、代理延迟、丢包率低
     家宽商宽不会被批哩批哩发觉

缺点:  不支持批哩批哩直播鸡（当然，如果你能成功配置并运行本项目，你一定能学会用OBS）

理想结果：
     如果主播和转播man的网络良好，使用YouTube跳板的延迟在10秒以下

本项目完全开源免费 如果你能找到合适的人做你的转播MAN，作者不收费
如果你没有合适的人选那么你可以联系作者使用作者的服务器，但是作者会收取费用 如有需求可以联系作者telegram： +12014648506

批哩批哩故意封锁海外、港澳台人直播（就算用中国身份证实名也不行）导致的，批哩批哩客服的说法是，由于技术原因某些地区无法直播  
既然是技术问题，就用技术解决嘛！

人员需求：肉身在海外的主播，肉身在中国的转播MAN（港澳台等批哩批哩不让你播的地方是不可以的）    
主播的软、硬件需求：同批哩批哩给的需求  
转播MAN的硬件需求：近10年出厂的个人电脑  
转播MAN的软件依赖：不老掉牙的Windows, Mac OS X 或Linux（小 心 a p t）,只要能运行 Python3, Streamlink1.3.1+, ffmpeg4+就行 连接速度10Mbps以上 丢包低的梯子 梯子越快越好
  
主播的准备工作  
  
注册一个youtube账号并申请直播，直播间选择Normal Latency（对梯子速度更友好 30s延迟 如果要求低延迟选择LL 10s或ULL 2s （对梯子要求较高））并关闭DVR， 在obs/Xsplit中填入youtube的直播链接和直播码（不支持批哩批哩直播鸡），向YouTube推流，并将YouTube直播间链接（注意不是studio.youtube.com的youtube直播设置页面）、你的批哩批哩直播链接、你的批哩批哩直播码告诉转播MAN  
  
  
  
转播MAN的工作  
  
首次运行前的配置工作
此教程仅适用windows 其他平台大同小异请自己解决  
下载本项目为zip并解压缩  
安装python 3  
	打开 https://www.python.org/downloads/ 下载并安装一个和你操作系统相符的python 3  
  
安装streamlink  
	打开https://github.com/streamlink/streamlink/releases/tag/1.4.1 下载并安装streamlink  
安装FFMPEG  
	打开https://ffmpeg.zeranoe.com/builds/ 下载ffmpeg  
	解压下载好的zip，打开并前往bin文件夹，将ffmpeg.exe复制粘贴到本项目的文件夹里  
配置工作完毕  
  
每次转播时的工作  
  
运行你用来看YouTube的梯子，并找到你梯子的http代理地址和端口（如果是本机则地址是http://127.0.0.1) 如果你找不到端口可以去问梯子的客服 
打开本项目文件夹，双击main.py运行  
在相应的地方填好代理地址和端口 （例格式：地址 http://127.0.0.1 端口 114 （不要照抄例子））
在相应的地方填好主播给你的YouTube直播间链接、批哩批哩直播链接、批哩批哩直播码  
点击start按钮

建议在第一次正式放送之前进行测试直播以免事故
作者不对使用本工具造成的放送事故负责
