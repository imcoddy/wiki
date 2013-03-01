输入法安装 http://bbs.baizhan.com.cn/viewthread.php?tid=158872
Root1.0.1 http://forum.xda-developers.com/showthread.php?t=1132693

8步重启法
能连电脑的话，可以用adb命令替代8步法，在winxp下试过可行
adb connect (nook ip)

adb shell 

echo -n -e "\x08\x00\x00\x00" > /rom/devconf/BootCnt

reboot


