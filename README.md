# <center><font face="仿宋" font color=orange>TASK 1</font>
## <center><font face="楷体" size=5>医电2403 曾一鸣</font></center>
| 电脑型号 | 网卡 | 显卡 |
| :---: | :---: | :---: |
| HUAWEI MateBook X Pro|AX211|无|

## <center><font face="仿宋" font color=red size=3>PS:由于装20.04时网卡无法驱动 在升级内核及安装iwlwifi后仍然如此，遂装了22.04</font></center>
## <center><font face="楷体" size=3>以下为安装流程汇报</font></center>
### 一、启动盘制作
#### 1、镜像文件及iso下载 :white_check_mark:
#### 2、启动盘制作
- 安装Ventoy :white_check_mark:
- 将iso导入启动盘 :x: :arrow_right: :white_check_mark:
  由于镜像文件过大（>4GB），而u盘本来的文件系统为**FAT32**，遂无法导入
  ![pAe9bid.jpg](https://s21.ax1x.com/2024/09/07/pAe9bid.jpg)
**<font color=red size=4>解决方案:</font>**
*备份u盘后将u盘格式化，并将文件系统转化为exFAT*
![pAe9vsf.jpg](https://s21.ax1x.com/2024/09/07/pAe9vsf.jpg)
### 二、安装系统的前期准备
#### 1、准备空间 :white_check_mark:
#### 2、关闭安全启动 :white_check_mark:
### 三、系统安装 :heavy_exclamation_mark:
<font color=red size=3>可正常安装系统，但无法连接网络（有线&无线）</font>
![pAeCPij.jpg](https://s21.ax1x.com/2024/09/07/pAeCPij.jpg)
![pAeC9oQ.jpg](https://s21.ax1x.com/2024/09/07/pAeC9oQ.jpg)
**:one:** 初步分析：可能是由于Linux内核版本过低(原本为5.15.0)而**无网卡驱动**导致    
**:two:** 尝试解决：在网络上下载较新版的**Linux内核文件**(先尝试了5.19.17，然后尝试了6.6.9)，以及**iwlwifi**驱动    
<font color=red size=3>......但仍然不管用 :cry: 甚至在安装6.6.9内核文件后卡在了启动界面</font>
![pAeCVyV.jpg](https://s21.ax1x.com/2024/09/07/pAeCVyV.jpg)
**:three:** 解决方案：认为是Linux版本过低导致，于是重新安装了**22.04** 问题解决 :white_check_mark:
