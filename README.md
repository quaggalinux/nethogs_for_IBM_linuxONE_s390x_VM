# nethogs_for_IBM_linuxONE_s390x_VM  
在IBM linuxONE s390x虚拟机上编译nethogs  
  
前端时间在IBM linuxONE s390x上开了一台Red Hat 8.4的虚拟机，结果发现很多常用工具都没有，可能因为是s390x的CPU指令集，没有小伙伴愿意编译到它上面运行  
最简单的是nethogs，在IBM linuxONE的库里面是没有的，就是不能用yum安装  
  
那只好自己动手编译了  
  
先登录到虚拟机，确定可以转到root用户，然后按照下面的命令无脑操作就行了  
#su  
#cd /  
#yum -y update  
#yum -y install make  
#yum -y install curl  
#yum -y install gcc  
#yum -y install gcc-c++  
#yum -y groupinstall 'Development Tools'  
#yum -y install wget  
#yum -y install nano  
#yum -y install cmake  
#yum -y install git  
#yum install ncurses-devel  
#yum install libpcap-devel  
  
在根目录建一个子目录，然后理论上git clone会先建一个目录再拉所有的文件树到这个自建的新目录里面  
#cd /  
#mkdir /s390  
#cd /s390  
  
拉项目下来，就是点项目右上角绿色的按钮“Code”，拷贝展开的URL路径粘贴到下面  
#git clone --recursive https://github.com/raboof/nethogs.git  
  
#cd nethogs  
  
按照项目编译要求的命令执行编译  
  
#make  
  
编译完成后nethogs运行文件在src目录里面  
  
#cd src  
  
#cp nethogs /usr/bin/  
  
完成后就可以愉快地玩耍了 ( *￣▽￣)o ─═≡※:☆  
  
