# ASUS-TUF-GAMING-B660-ATX-OPENCORE-EFI
## 一、配置
```bash
主板:华硕TUF GAMING B660 WIFI D4
CPU:INTEL i7 12700
内存:芝奇皇家戟F4-3600C18D  32G(16GX2)
电源:长城G6 650W金牌全模组
硬盘:西数SN850 500G (macOS)  铠侠RC20 500G (WIN) 三星PM981A 512G (GAME)
散热:九州风神大霜塔
机箱: 先马鲁班1
显卡:蓝宝石RX6600XT 超白金
风扇:利民TL-B12WS X4
```

![image](https://user-images.githubusercontent.com/35289289/179716053-05308723-a524-47ea-9618-e56740146c4a.png)

![image](https://user-images.githubusercontent.com/35289289/179716209-24d0f839-8bc9-4199-ac34-2a6a4e64aed6.png)

![image](https://user-images.githubusercontent.com/35289289/179717138-f7491f23-e60b-4493-8b1a-16848f9fa862.png)

![image](https://user-images.githubusercontent.com/35289289/179717256-532b2cf9-3ce0-4ffc-887b-24be4c6e012f.png)




## 二、opencore版本

`0.8.2`

## 三、安装
1、windows下使用balenaEtcher


![image](https://user-images.githubusercontent.com/35289289/179437830-6b79fa28-0e0a-4017-80d5-4fe905119b22.png)



2、balenaEtcher烧录dmg镜像到U盘

![image](https://user-images.githubusercontent.com/35289289/179437874-e2c4c847-bdff-4edb-92df-31e7e832eb42.png)

安装好之后，通过diskgenius或者在mac下手动挂载U盘的EFi分区，可以把现成的EFI文件夹拷贝到U盘的EFi分区
如下文件结构

![image](https://user-images.githubusercontent.com/35289289/179437915-84abde54-5082-4e6d-863b-277095464b5e.png)

![image](https://user-images.githubusercontent.com/35289289/179437934-c34eca50-4e66-4c11-a198-64cd74408c9b.png)


3、bios调整

![image](https://user-images.githubusercontent.com/35289289/179437986-0b766cd2-ecda-400f-88bf-304861b01649.png)


开机F2进入到bios
按F7到高级
关闭快速启动


![image](https://user-images.githubusercontent.com/35289289/179438057-ed9c439c-8c43-4714-ba91-1bb802d6e9e0.png)


禁用CSM（默认都是关闭的，但是还是检查下）

![image](https://user-images.githubusercontent.com/35289289/179438094-c3a56991-fe57-4548-a2b1-e9a4b65a562d.png)


禁用串口

![image](https://user-images.githubusercontent.com/35289289/179438136-b70dc456-27a3-4ce7-bf6f-4cecfe08c5b5.png)


安全启动菜单
这里安全启动菜单实测不需要改，保持如下默认即可


![image](https://user-images.githubusercontent.com/35289289/179438173-cdc2fd3b-6b7e-4c41-8408-636f3875354a.png)



4、重启按F8选择使用U盘启动

如果以下在安装中出现鼠标跟键盘来回滚动的图片，说明当前鼠标跟键盘无法被识别，如果当前插在了主板后面可以换到机箱前置面板下试下


![image](https://user-images.githubusercontent.com/35289289/179438218-ae3eaf81-8df4-4660-9c6f-37a74cea17bd.png)


进入磁盘工具，点击上方菜单栏选显示所有设备
然后对磁盘进行抹掉，apfs分区，guid分区图即可，此次是整个磁盘作为mac系统使用


![image](https://user-images.githubusercontent.com/35289289/179438243-c7d9df3e-8fab-469c-9160-c31082aa6cbe.png)


退掉磁盘工具，点开始安装

![image](https://user-images.githubusercontent.com/35289289/179438294-d40ad5ae-b1a8-41b5-9bdb-ab6fa7d66dac.png)



![image](https://user-images.githubusercontent.com/35289289/179438327-20b02d02-2b44-41f6-bcbc-0dd08ed38972.png)



从以上这个剩余多少时间开始
进度条跑完安装完macos会第一次重启，
u盘插在上面
出现macos安装盘再重启一次
跑一段代码再重启一次
以上都是自动重启无需手动去点
然后会遇到一种情况，机器重启多次，至少重启了5次，屏幕上没有任何显示，顶多显示没有信号，但是没有mac相关的界面，这种情况就需要手动点按机箱上的重启按钮，手动重启
手动重启之后如下图：

![image](https://user-images.githubusercontent.com/35289289/179438369-668613bf-8047-4f47-8df0-7fc87e8bee3b.png)



## 四、完善情况
1、睡眠正常，机箱电源按钮进行唤醒

2、metal功能集正常

![image](https://user-images.githubusercontent.com/35289289/179439288-d9abbe70-b671-49f8-b920-5ab566805ae8.png)

3、硬解正常

![image](https://user-images.githubusercontent.com/35289289/179439367-25dec9b0-4f14-4f4d-9299-3a3e1de2de6c.png)

4、板载网卡Intel(R) Ethernet Controller (3) I225-V (10.0.80.26)在macOS 12.4驱动正常，可正常上网

![image](https://user-images.githubusercontent.com/35289289/179714931-5e2f975a-d8f1-42e4-a129-761c944513e7.png)


5、声卡正常

![image](https://user-images.githubusercontent.com/35289289/179715047-0d246098-83c7-4a98-8719-033455e121c7.png)




6、无线wifi以及蓝牙未测试

## 五、跑分

![image](https://user-images.githubusercontent.com/35289289/179439060-e070034c-35a8-4adb-aec3-c39b3312026f.png)


![image](https://user-images.githubusercontent.com/35289289/179439086-a62dc1b5-56a4-4605-9a63-fbae5be58b64.png)













