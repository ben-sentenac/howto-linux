# Format usb key 

1. Indentify usb key with:

```sh 
lsblk
```
ou 

```sh 
sudo fdisk -l
```
ou

```sh 
 df
```
you 'll see a list of devices, your usb will be something like /dev/sdx (replace x by the corresponding letter to your key)

2. Unmount usb key 

```sh 
sudo umout /dev/sdx*

```
## Write an iso image:

```sh
sudo dd if=/chemin/vers/kali-linux.iso of=/dev/sdX bs=4M status=progress
```

- `if=/chemin/vers/kali-linux.iso` : full path to iso file.
- `of=/dev/sdX` : Replace X by corresponding letter of usb key.
- `bs=4M` : set block size to speed up the process.
- `status=progress` : display progress status.

then synchronize system:
```sh
sudo sync
```