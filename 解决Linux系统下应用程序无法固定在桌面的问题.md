## 解决Linux系统下应用程序无法固定在桌面的问题

#### 问题描述

部分应用程序如jetbrain公司的clion编译器下载后无法固定在桌面，只能通过命令行运行.sh文件启动，十分麻烦。

#### 解决办法

新建一个后缀为.desktop的文件，用文本编辑器gedit打开，添加如下脚本：

`[Desktop Entry]`

`Encoding=UTF-8`

`Name=xxx`

`//可执行文件`

`Exec=sh  /usr/local/src/xxx/target/build/bin/startup.sh       //.sh可执行文件的绝对路径, 前面的sh 命令不要丢哦`

`Icon=/usr/local/share/icons/jesh.png  //图标图片路径，更改这里即可`

`Info="Spark"`

`Categories=GTK;Network;message; //可写可不写`

`Comment="Gtk+ based like QQ"  //提示性信息 ，可写可不写`

`Terminal=false`

`Type=Application`

`StartupNotify=true`

然后更改文件的权限：

`sudo chmod 755 name.desktop`

输入密码之后，就可以直接点击你所创建的图标**启动应用**了

移动文件到`/usr/share/applications/`下
最后在Ubuntu自带的搜索框内搜索就可以直接将应用**放在启动栏**了