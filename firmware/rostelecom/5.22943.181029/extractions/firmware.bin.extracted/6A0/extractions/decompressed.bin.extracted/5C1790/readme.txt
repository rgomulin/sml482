binwalk достал нам из прошивки ядро и расжал его в файл decompresed.bin

натравим ня ядро еще раз binwalk:
~/.cargo/bin/binwalk -y cpio -e decompressed.bin

и получим распакованную директорию с initramfs
запакуем ее содержимое и сохраним тут, пусть будет в отдельном виде
tar czf initramfs.cpio.gz *

