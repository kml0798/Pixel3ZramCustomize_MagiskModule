# Pixel3ZramCustomize_MagiskModule
一个用于pixel3的zram设置magisk模块，可以通过修改/system/vendor/etc/fstab.sdm45中的zramsize来修改默认zram大小（测试平台为pixel3 android12(SP1A.210812.016.C2)）


如果需要自定义大小或者平台，请首先查看/system/vendor/etc下是否存在“fstab.平台代号”文件，并打开寻找zram，确定存在相应的代码设置后，将此文件复制出来并且进行修改，如果找不到，这里提供一个方法：


/system/vendor/etc/init/hw 里可能存在一个类似init.平台代号.rc 的文件，打开查找zram字段，可能在这里可以找到zram设置文件路径，我就是这样找到的zramsize设置文件
