с помощью binwalk3 извлекаем содержимое firmware.bin:

---------------------------------------------------------------------------------------------------------------------------------------------
DECIMAL      HEXADECIMAL   DESCRIPTION
---------------------------------------------------------------------------------------------------------------------------------------------
1696         0x6A0         gzip compressed data, original file name: "vmlinux", operating system: Unix, timestamp: 2018-10-29 08:23:01, total
                           size: 3997538 bytes
4000044      0x3D092C      SquashFS file system, little endian, version: 4.0, compression: gzip, inode count: 909, block size: 131072, image
                           size: 49790847 bytes, created: 2018-10-29 08:23:07
53791828     0x334CC54     CramFS filesystem, little endian, 11 files, total size: 20480 bytes
---------------------------------------------------------------------------------------------------------------------------------------------

в составе rootfs есть загрузчик
3D092C/squashfs-root/usr/share/cfe.bin
и в нем не залочена консоль. Пригодится
