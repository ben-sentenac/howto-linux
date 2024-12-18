# Linux File System Hierarchy

Linux follows a standardized directory structure defined by the Filesystem Hierarchy Standard (FHS). Below is an overview of the main directories and their purposes.

---

## 1. `/` - Root Directory
- The top-level directory of the Linux file system.
- All other directories are contained within `/`.

---

## 2. `/bin` - Essential User Binaries
- Contains binaries or user executable files which are available to all users
- essential command-line programs needed for booting and basic functionality.
- Examples: `ls`, `cp`, `mv`, `bash`.

---

## 3. `/sbin` - System Binaries
- Contains essential system administration binaries.
- Examples: `fsck`, `reboot`, `iptables`.

---

## 4. `/etc` - Configuration Files
- Stores system-wide configuration files.
- Examples:
  - `/etc/passwd`: User account information.
  - `/etc/fstab`: File system mount points.

---

## 5. `/dev` - Device Files
- Contains device nodes that represent hardware devices.
- Examples:
  - `/dev/sda`: First hard disk.
  - `/dev/tty`: Terminals.

---

## 6. `/proc` - Process Information
- A virtual file system providing runtime system information.
- Examples:
  - `/proc/cpuinfo`: CPU information.
  - `/proc/meminfo`: Memory usage.

---

## 7. `/sys` - System Information
- Another virtual file system providing information about the system and kernel.
- contains information about devices, drivers, and some kernel features

---

## 8. `/var` - Variable Data
- Stores data that changes frequently, such as:
  - Logs: `/var/log`
  - Spools: `/var/spool`
  - Cache files: `/var/cache`

---

## 9. `/tmp` - Temporary Files
- Used for storing temporary files.
- Files here are typically deleted on reboot.

---

## 10. `/usr` - User Programs
- Contains user-related programs and libraries.
- Key subdirectories:
  - `/usr/bin`: User binaries.
  - `/usr/lib`: Libraries for user binaries.
  - `/usr/share`: Shared data like icons, documentation.

---

## 11. `/home` - User Home Directories
- Stores personal files for each user.
- Example: `/home/username`

---

## 12. `/boot` - Bootloader Files
- Contains files needed to boot the system.
- Examples:
  - Kernel: `/boot/vmlinuz`
  - Bootloader: `/boot/grub`

---

## 13. `/lib` - Essential Libraries
- Stores shared libraries needed by binaries in `/bin` and `/sbin`.

---

## 14. `/opt` - Optional Software
- Used for installing optional or third-party software packages.

---

## 15. `/mnt` - Temporary Mount Points
- Used for temporarily mounting file systems.

---

## 16. `/media` - Removable Media
- Mount points for removable media like USB drives and CDs.

---

## 17. `/root` - Root User's Home Directory
- The home directory for the root (superuser) account.

---

## 18. `/run` - Runtime Data
- Holds temporary runtime data for system processes.

---

## 19. `/srv` - Service Data
- Stores data for specific services like web servers (`/srv/www`).

---

This hierarchy provides a standardized way to organize files and directories in Linux, ensuring a consistent structure across distributions.
