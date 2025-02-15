core.img for x86_64

to create a bootable iso that runs the executable file for the x86_64 architecture.

located in /bootable

run the command:

```
 mkisofs -R -V "EXECUTABLE" -b boot/grub/core.img -no-emul-boot -boot-load-size 4 -boot-info-table -o salida.iso iso iso
```

```
sudo mount -o loop salida.iso /mnt/iso
```
