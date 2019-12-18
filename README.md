# BurpSuite-jar2app-mac
Give the way to crack Burp Suite Professional 2.* and launch it as a Mac OS X app.

## 准备所需文件

1. 下载Burp Suite Professional 2.1.06 jar包和loader文件
- [burpsuite_pro_v2.1.06.jar](https://github.com/Mr-xn/BurpSuite-collections/releases/download/2.1.06/burpsuite_pro_v2.1.06.jar)  - `MD5: fe961272897736d37a2eab4cdb048416`
- [burp-loader-keygen-2_1_06.jar](https://github.com/Mr-xn/BurpSuite-collections/releases/download/2.1.06/burp-loader-keygen-2_1_06.jar)


2. 使用以下命令安装[jar2app](https://github.com/Jorl17/jar2app)，Cartalina需要安装到/usr/local/bin目录

```bash
$ git clone https://github.com/Jorl17/jar2app
$ cd jar2app
$ chmod +x install.sh uninstall.sh
$ sudo ./install.sh /usr/local/bin
```

## 进行app转换

1. 使用jar2app将jar文件转换成app，并设置包名称、菜单显示名称、传统菜单、以及loader参数
```bash
$ cd /path/to/*burpsuite_pro_v2.1.06.jar所在位置*
$ jar2app -i app.icns burpsuite_pro_v2.1.06.jar -j "-noverify -Xbootclasspath/p:/\$APP_ROOT/Contents/Java/burp-loader-keygen-2_1_06.jar" -o -n "Burp Suite Professional" Burp\ Suite\ Professional
```

2. 复制loader至app包内
```bash
$ cp /path/to/*burpsuite_pro_v2.1.06.jar所在位置* /path/to/*生成的Burp Suite Professional.app所在位置*/Contents/Java/
```

## 进行破解
至此app封装完成，将程序复制到mac应用程序文件夹内，按照标准操作进行注册即可，注册过程可以参考[四爷的文档](http://scz.617.cn:8/misc/201910151519.txt)，之后无需命令行引导程序，直接双击就可以启动burpsuite了。
