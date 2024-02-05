### 1、为什么要用双机调试？

![](..\images\01\微信截图_20240205163803.png)

**在本机安装 windbg**

**虚拟机里面装 XP系统**



### 2、配置双机调试流程

1、在本机安装windbg

2、在虚拟机中XP，修改boot.ini

3、设置虚拟机

4、修改windbg运行参数，指向虚拟机



### 3、在虚拟机XP中修改boot.ini

multi(0)disk(0)rdisk(0)partition(1)\WINDOWS="Microsoft Windows XP Professional[debug]" /execute=optin /fastdetect /debug /debugport=com1



### 4、为XP虚拟机添加一个串口

![](..\images\01\微信截图_20240205165049.png)

![](..\images\01\微信截图_20240205165314.png)



### 4、修改 windbg  运行参数，指向虚拟机

-b -k com:port=\\\\.\pipe\com_1,pipe

![](..\images\01\微信截图_20240205165831.png)

