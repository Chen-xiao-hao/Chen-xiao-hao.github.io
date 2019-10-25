# 戴尔笔记本如何安装Ubuntu18.04与Win10双系统

当一个计算机小白尝试安装双系统，感受就两个字：自闭。

我的电脑是Dell==酷睿i5-8265==，以此为例规避一下我踩过的坑。

## 一、制作Ubuntu18.04系统U盘启动盘

这部分可参考https://blog.csdn.net/qq_38153833/article/details/86505612

## 二、分盘

右键此电脑→管理→磁盘管理→找一个容量够的盘，右键，点击压缩卷→输入要压缩的空间大小（这里依自身情况而定），点击压缩即可。完成后，你会看见有一个显示未分配的盘。

## 三、改BIOS

这是Dell最磨人的坑了……

重启电脑，在Dell图标出来前持续一下一下地按F2，顺利进入BIOS

双击System Configuration，点击SATA Operation，选择AHCI，然后右下角apply即可。

![QQ图片20191025213856](C:\Users\提拉米苏\Desktop\陈小浩\Blue-Whale\第二次作业\QQ图片20191025213856.jpg)

## 四、安装Ubuntu

OK，现在进入windows，插入系统盘，点击开始→设置，

![QQ图片20191025220540](C:\Users\提拉米苏\Desktop\陈小浩\Blue-Whale\第二次作业\QQ图片20191025220540.png)

再选择更新和安全，

![QQ图片20191025220446](C:\Users\提拉米苏\Desktop\陈小浩\Blue-Whale\第二次作业\QQ图片20191025220446.png)

点击左侧一栏中的恢复→高级启动，点击 立即重新启动……

![QQ图片20191025142243](C:\Users\提拉米苏\Desktop\陈小浩\Blue-Whale\第二次作业\QQ图片20191025142243.jpg)

点击使用设备，就可以Install Ubuntu18.04了。

具体安装过程可参照https://blog.csdn.net/qq_35379989/article/details/78934785

## 五、后续操作

（如果安装完成后，你发现SATA选择AHCI 时，只能进入Ubuntu而进不了windows；选择RAID On时，只能进windows而进不了Ubuntu，，那就按照此步骤操作一下叭。。）

再次进入windows，选择高级启动中的立即重新启动

![QQ图片20191025142227](C:\Users\提拉米苏\Desktop\陈小浩\Blue-Whale\第二次作业\QQ图片20191025142227.jpg)

这次选择疑难解答→高级选项→启动设置→启动→按F4进入安全模式。

右键此电脑→管理→点击左侧的设备管理器→中间一栏的显示适配器→右键第二个，选择禁用设备（禁独显）

![IMG_20191025_225607](C:\Users\提拉米苏\Desktop\陈小浩\Blue-Whale\第二次作业\IMG_20191025_225607.jpg)

重新启动，看看能不能在windows和ubuntu之间自由切换，，如果可以了，再按上述操作步骤，开独显就OK了。