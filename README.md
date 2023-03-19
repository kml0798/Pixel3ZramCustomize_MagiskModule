# Pixel3ZramCustomize_MagiskModule

一个用于pixel3的zram设置magisk模块，可以通过修改/system/vendor/etc/fstab.sdm45中的zramsize来修改默认zram大小（测试平台为pixel3 android12(SP1A.210812.016.C2)），实测后台保活能力大幅提升，但由于zram压缩特性可能导致切换应用出现部分卡顿，通常认为zram设置过大反而会造成内存资源过度占用等问题，但暂时没有发现类似非常严重的问题
----

<font color=#feb3ab>如果需要自定义大小或者平台，请首先查看/system/vendor/etc下是否存在“fstab.平台代号”文件，并打开寻找zram，确定存在相应的代码设置后，将此文件复制出来并且进行修改，如果找不到，这里提供一个方法：</font>


/system/vendor/etc/init/hw 里可能存在一个类似init.平台代号.rc 的文件，打开查找zram字段，可能在这里可以找到zram设置文件路径，我就是这样找到的zramsize设置文件


![image](https://github.com/kml0798/Pixel3ZramCustomize_MagiskModule/blob/main/ProjectImage/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20230319123532.jpg)





![image](https://github.com/kml0798/Pixel3ZramCustomize_MagiskModule/blob/main/ProjectImage/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20230319123519.jpg)


`默认大小为2147483648（2GB），因为感觉后台保活能力很差，所以改为4294967296（4GB）`


![image](https://github.com/kml0798/Pixel3ZramCustomize_MagiskModule/blob/main/ProjectImage/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20230319125619.jpg)
