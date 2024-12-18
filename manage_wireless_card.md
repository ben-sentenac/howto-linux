
# How to see your network Interfaces:
look for network interfaces:
```sh
sudo ifconfig
```
or
```sh
ip link
```
or for wireless

```sh
sudo iw dev
```
Look for interfaces like wlan0, wlan1, etc.
2. 

# How to Put Your Wireless Card into Monitor Mode

This guide explains how to put your wireless card into monitor mode using various methods, including `iw`, `iwconfig`, and `airmon-ng`.

---

## 1. Check Wireless Card Compatibility

Not all wireless cards support monitor mode. Verify if your card supports it by running:
```bash
iw list
```
or

```sh
sudo iwconfig <interface>

```

## 2 . Disable the Wireless Interface:

```sh 
sudo ifconfig <interface> down

```
or

```sh
sudo ip link set <interface> down
```

## 3. Set the Interface to Monitor Mode:

```sh
sudo iw <interface> set type monitor
```
or 

```sh 
sudo iwconfig <interface> mode monitor
```

## 4. Enable the Wireless Interface

```sh 
sudo ifconfig <interface> up
```
or 

```sh 
sudo ip link set <interface> down
```

## 5. Verify the Mode:

You should see Mode:Monitor for your wireless interface.

```sh
sudo iwconfig <interface>
```
or

```bash
iw list
```

## 6. Using airmon-ng (Alternative Method):

The `airmon-ng` tool (part of the aircrack-ng suite) can simplify enabling monitor mode.


```sh 
sudo apt update
sudo apt install aircrack-ng
# start monitor mode:
sudo airmon-ng start <interface>
#to stop monitor mode:
sudo airmon-ng stop <interface>
```

