# Lighthouse-Monitor
监控腾讯云轻量应用服务器，实现状态推送，流量超限自动关机，流量充足自动开机。

### 1.简介

监控腾讯云轻量应用服务器流量使用情况，流量超限自动关机，流量充足自动开机，并推送至多平台。

注意：脚本主要参考[@2lifetop](https://github.com/2lifetop/LightHouse_Automatic_Shutdown)的项目！！！

### 2.获取密钥
访问https://console.cloud.tencent.com/cam/capi

建议使用子账户，点击快速创建，访问方式改为【编程访问】

![](https://997888.xyz/ImageHosting/69.png)
![](https://997888.xyz/ImageHosting/70.png)
![](https://997888.xyz/ImageHosting/71.png)

用户权限改为【QcloudLighthouseFullAccess】

记得取消【AdministratorAccess】，这样，即使泄露密钥也不会对账号内其他业务产生影响。

![](https://997888.xyz/ImageHosting/72.png)
![](https://997888.xyz/ImageHosting/73.png)

将【SecretId】【SecretKey】复制。并填入脚本中

### 3.配置推送
执行一次脚本就会将实例的状态（包括ID、流量、运行状态）推送至指定平台（默认仅推送至Bot）。不喜欢这个功能可以注释掉70-78行
![](https://997888.xyz/ImageHosting/74.png)

当执行开机，关机操作时，会推送至指定平台（默认为Bot和Server酱）。

Bot推送，替换掉token，详见https://dianbao.vercel.app

Server酱推送，请在引号内填入你的SendKey，详见https://sct.ftqq.com/sendkey

qmsg酱推送，替换掉token，详见https://qmsg.zendee.cn

![](https://997888.xyz/ImageHosting/75.png)

### 4.效果

![](https://997888.xyz/ImageHosting/76.png)














