Debian5 (lenny)上安装的python是2.5的，很老，怎么安装2.7的呢？
除了编译之外，我们还可以用apt的方法搞定。如下：

1、修改源
实际上python2.7在unstable源中

1
sudo vim /etc/apt/sources.list
2
#添加
3
deb http://ftp.us.debian.org/debian/ unstable main contrib non-free
4
 
5
#更新
6
sudo apt-get update
2、安装

1
sudo apt-get install python2.7
3、替换

1
sudo rm /usr/bin/python
2
sudo ln -s /usr/bin/python2.7 /usr/bin/python

