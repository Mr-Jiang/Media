# Media
利用TCP/IP、UDP、Http、Socket、多线程等实现局域网实时监控、文件快传、搜索设备等

# CSDN博客地址
https://blog.csdn.net/jspping/article/details/79774375

# 效果图
![image](https://github.com/Mr-Jiang/Media/blob/master/MediaImage/mediaImage.png)

# 效果视频下载地址
http://www.engineer-jsp.cn/docs/MediaVideo.MOV

# Usage

1.将MediaPushServer.apk安装好并打开热点或将他俩(服务端与客户端)处于同一WIFI网络下

2.将安装MediaRecvClient.apk的手机连接安装MediaPushServer.apk的手机热点或或将他俩(服务端与客户端)处于同一WIFI网络下

3.打开MediaPushServer单击“开始推送”按钮，Toast提示“开始推送”表示推送开始，单击“关闭推送”可关闭推送

4.打开MediaRecvClient+，单击“开始”按钮，会优先尝试连接路由器5次，每5s/次，连接失败后开始尝试局域网搜索设备，扫描15次，每2s/次，成功扫到至少一个设备时，弹出设备列表，选择一个item设备可进行连接，单击“取消”按钮可取消本次搜索

主要的模块大致就是这些，它们的主要职能也介绍了，下面简单介绍项目的一些注意事项。

# 注意事项：

1.关于服务端在部分机型上无法调起Camera导致黑屏的问题，这个问题我在三星、华为机型上发现了，但是没有处理，因为我查看了这些机型的预览配置、图片大小配置，因为博主设置的参数值是在配置范围内的，所以这个问题博主没有去深究，暂时未找到引起异常的原因

异该常为：java.lang.RuntimeException: setParameters failed

很诡异，笔者设置的参数都是机型支持的合法值范围，但还是报这个异常，但如果不设置Camera.setParameters()参数会出现一系列的花屏、绿屏等问题

2.关于将apk安装在平板时的问题，部分平板可能没有imei号，导致程序读取异常并崩溃，建议安装在手机上

3.局域网内连接的情况下，由于硬件或网络通路问题会导致画面偶尔卡顿，获取文件目录过久，建议安装了MediaPushServer的手机打开热点，客户端连接这个热点，通信效果最佳

# License
Copyright (C) 2018 Engineer-Jsp<br><br>
Licensed under the Apache License, Version 2.0 (the "License");<br>
you may not use this file except in compliance with the License.<br>
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
