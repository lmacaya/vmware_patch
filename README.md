# vmware_patch

##Enable shared folders on VMWare Fusion 7.0.0 for Ubuntu 14.04.2

##Download inode-vmhgfs.patch and file-vmhgfs.patch patches.

>cd ~
>git clone https://github.com/lmacaya/vmware_patch/

##Use vmware-tools compilation file patches

>cd /usr/lib/vmware-tools/modules/source/
>sudo tar xf vmhgfs.tar
>cd vmhgfs-only
>sudo patch inode.c < ~/inode-vmhgfs.patch
>sudo patch file.c < ~/file-vmhgfs.patch
>sudo tar cf vmhgfs.tar vmhgfs-only

##Set vmware-tools configuration

>sudo vmware-config-tools.pl -d

##Add Shared Folder

Virtual Machine / Share / Settings - Share

Thanks to: "Scott M. Kroll" <skroll@gmail.com>
