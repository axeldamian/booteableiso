core.img for x86_64

to create a bootable iso that runs the executable file for the x86_64 architecture.

located in /bootable

You must be located where the /iso folder is, you must view it.

run the command:

```
 mkisofs -o programa.iso -V "Programa" -b boot/grub/core.img -no-emul-boot -boot-load-size 4 -boot-info-table -R -J -graft-points ./iso
```

```
sudo mount -o loop salida.iso /mnt/iso
```

```
isoinfo -d -i programa.iso
```

you will see something like this::
```
CD-ROM is in ISO 9660 format
System id: Mac OS X
Volume id: Programa
Volume set id:
Publisher id:
Data preparer id:
Application id: MKISOFS ISO9660/HFS/UDF FILESYSTEM BUILDER & CDRECORD CD/DVD/BluRay CREATOR (C) 1993 E.YOUNGDALE (C) 1997 J.PEARSON/J.SCHILLING
Copyright File id:
Abstract File id:
Bibliographic File id:
Volume set size is: 1
Volume set sequence number is: 1
Logical block size is: 2048
Volume size is: 294
El Torito VD version 1 found, boot catalog is in sector 36

Joliet with UCS level 3 found.
SUSP signatures version 1 found
Rock Ridge signatures version 1 found
Rock Ridge id 'RRIP_1991A'
Eltorito validation header:
    Hid 1
    Arch 0 (x86)
    ID ''
    Cksum AA 55 OK
    Key 55 AA
    Eltorito defaultboot header:
        Bootid 88 (bootable)
        Boot media 0 (No Emulation Boot)
        Load segment 0
        Sys type 0
        Nsect 4
        Bootoff 25 37
```