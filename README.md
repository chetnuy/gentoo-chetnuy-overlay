### Gentoo custom overlay of Chetnuy

## dev-util/arch-install-scripts
This packages need for archiso on gentoo 

Gentoo install:
layman -o https://raw.github.com/chetnuy/gentoo-chetnuy-overlay/master/repositories.xml -f -a gentoo-chetnuy-overlay
sudo emerge -av squashfs-tools libisoburn dosfstools lynx arch-install-scripts
sudo echo "Server = http://mirror.yandex.ru/archlinux/$repo/os/$arch > /etc/pacman.d/mirrorlist"

Setting /etc/pacman.conf file
uncommited: 
XferCommand = /usr/bin/wget --passive-ftp -c -O %o %u
and add everything section [core,community,...]
SigLevel = Required DatabaseNever
```

Last instruction basement on https://gist.github.com/satreix/c01fd1cb5168e539404b, but fewmoments for gentoo (@)
'''
git clone git://projects.archlinux.org/archiso.git && cd archiso
sudo make install && cd .. && rm -rf archiso
mkdir ~/livecd
sudo cp -r /usr/share/archiso/configs/releng/* ~/livecd && cd ~/livecd
@ edit ./livecd/pacman.conf as /etc/pacman.conf
./build.sh -v

```

