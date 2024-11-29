# AddingDiskToUbuntu
===================================AddingNewDiskToUbunt===================================
    sudo reboot now //da ucitamo novu particiju
    lsblk
===================================parted===================================
    sudo parted /dev/sdb
    (parted) mklabel gpt
    (parted) unit TB
    
    (parted) mkpart
    Partition name?  []? primary
    File system type?  [ext2]? ext4
    Start? 0%
    End? 100%

    (parted) print
    (parted) quit
===================================fdisk===================================  
    sudo mkfs -t ext4 /dev/sdb1
    
===================================fdisk=================================== 
    sudo mkdir /media/mynewdrive
    sudo mount /dev/sdb1 /media/mynewdrive 
    sudo vi /etc/fstab  ===>  /dev/sdb1    /media/mynewdrive   ext4   defaults     0        2
