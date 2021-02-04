# hackKernel

## 安装5.10.12版本Linux kernel（可选，根据需求调整）
前往

https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.10.12/

下载两个header、module和image的deb文件，安装：

sudo dpkg -i *.deb

sudo reboot

uname -r确认内核版本为5.10.12

bug:

https://www.spinics.net/lists/kernel/msg3716600.html

## 卸载kernel
sudo dpkg -l | grep linux

sudo dpke -r XXXX

-r删除不掉的文件使用--purge

## 查看kprobes开关
echo /sys/kernel/debug/kprobes/enabled

1为开，0为关

## 查看内核函数
cat /proc/kallsyms | grep _do_fork

T   The symbol is in the text(code) section

D   The symbol is in the initialized data section

R   The sysbol is in a read only data section

t   static

d   static

R   const

r   static const

