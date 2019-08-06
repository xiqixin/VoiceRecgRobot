# VoiceRecgRobot
语音AI识别管理工具

## 项目简介
    使用C++编写一个智能AI对话和语音命令执行的工具
    同时还支持配置指定命令

## 项目技术点
     C++STL
     http第三方库
     图灵机器人
     百度语音识别和语音合成
     linux系统/网络编程
     第三方库与第三方工具的安装与使用

## 项目演示
     程序启动之后先加载配置文件，启动本地录音工具，进行录音
     程序将语音录制到本地，使用百度语音识别平台进行识别，将识别得到的文字信息与配置文件进行比对
     判断是普通对话还是命令
     如果是命令，则执行相应的命令完成一次语音命令执行
     如果是普通对话信息，推送给图灵机器人进行智能对话，得到图灵机器人响应的文本，调用百度语音合成
     在本地合成语音，用相应地语音播放工具播放语音信息完成对话信息，完成语音对话功能
    
## 项目准备
### 1.使用图灵机器人，官网：http://www.turingapi.com/
       在该网站注册一个图灵机器人并进行认证，具体使用可以查看机器人api使用文档
### 2.注册百度语音识别，上官网：http://ai.baidu.com/
       在语音识别模块创建应用，具体使用查看技术文档（C++SDK下载和语音识别的使用）
### 3.准备第三方库和SDK
####  （1）安装高版本gcc
          # sudo yum install centos-release-scl 
          # sudo yum install devtoolset-6 
          # scl enable devtoolset-6 bas
####  （2）下载百度C++语音识别SDK
           在http://ai.baidu.com/sdk下载
####  （3）安装jsoncpp，要求：>1.6.2版本，0.x版本将不被支持 
           json官网：http://www.json.org/json-zh.html 注意，
           推荐使用https://github.com/open-source-parsers/jsoncpp/releases 1.8.3版本，
           其他最新版本可能会有中 文编码的问题
####  （4）安装openssl 
           # sudo yum install openssl-devel
####  （5）安装libcurl（需要支持https）
           官网：<https://curl.haxx.se/download.html 下载curl-7.64.1.tar.gz版本
           # tar xzf curl-7.64.1.tar.gz 
           # cd curl-7.64.1 
           # ./configure 
           # make 
           # sudo make install
### 4.准备Centos 7 录音和播放工具
       安装SMplayer-->https://blog.csdn.net/longzhutengyue/article/details/84782330
