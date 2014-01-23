clouder
=======
Tool for create qcow2 or raw image with Ubuntu, RHEL, CentOS.
You can easily create custom-size image.

###WARNING: 
     Do not interrupt clouder. It may crush system

###NAME
     clouder — simple tool for creating OS-image for qmeu kvm, lxc-container OR eine.

###SYNOPSIS
     clouder [osVersion] [<advanced options>]

###OPTIONS
     -r — size of root file system in Megabytes. Minimal size for supported os - 700
     Megabytes
     -f — type of filesystem. Supported types: ext2, ext3, ext4, minix, msdos, vfat, by
     default is ext3
     -s — size of swap in Megabytes
     -v — version of Operating system. Supported os: precise, lucid, centos-6, slc-6
     -o — output format: raw, qcow2, tar.gz. By default is raw
     -O - output file: without output format extension. By default is "./os.img"
     -p — password: set root-password. By default is qwerty
     -S — user script to execute into created operating system
     -h — hostname for created operating system. By default is localhost

###RESULT
     Custom format image with any size, fs or type of OS version, configured by yourself

###LOGS
     /var/log/clouder/*.log

###EXAMPLES
     clouder -v precise
     clouder -r 1500 -f ext4 -v centos-6 -h leo.devfol.qa.yandex.net
     clouder -r 800 -f ext2 -s 300 -v precise -o tar.gz -h leo.devfol.qa.yandex.net -p myPass
     clouder -r 800 -f ext4 -s 300 -v lucid -o qcow2 -O /var/lib/myImage -h leo.devfol.qa.yandex.net -p myPass

###AUTHOR
     leo - leoleovich@yadex-team.ru
