# wifi-manager
A command-line tool for managing Wi-Fi in Mac OS X

```
usage: wifi-manager [-h] [-v] [-i INTERFACE]
                    {preferred,scan,connect,disconnect,status,info,mac,power}
                    ...

A command-line tool for managing Wi-Fi in Mac OS X

positional arguments:
  {preferred,scan,connect,disconnect,status,info,mac,power}
                        available commands
    preferred           list preferred networks
    scan                scan for networks
    connect             connect to a network
    disconnect          disconnect from a network (requires root privilege)
    status              show network connection status
    info                show connected network info
    mac                 show device hardware (MAC) address
    power               control device power state

optional arguments:
  -h, --help            show this help message and exit
  -v, --version         show program's version number and exit
  -i INTERFACE          specify Wi-Fi device to use
```

## Install
```
git clone https://github.com/tuladhar/wifi-manager
cd wifi-manager
install -m 755 wifi-manager /usr/local/bin
```

## Scan for networks
```
$ wifi-manager scan
```

## Connect to an insecure network
```
$ wifi-manager connect --help

usage: wifi-manager connect [-h] network password

positional arguments:
  network     network name
  password    network password

optional arguments:
  -h, --help  show this help message and exit
```

```
$ wifi-manager connect "insecure-network" ""
```

## Connect to a protected network
```
$ wifi-manager connect "protected-network" "password"
```

## Disconnect from a connected network
```
$ sudo wifi-manager disconnect
```

## Control Wi-Fi Power
```
$ wifi-manager power status
Wi-Fi device en1 is currently powered on
```

```
$ wifi-manager power off
Wi-Fi device en1 powered off
```

```
$ wifi-manager power on
Wi-Fi device en1 powered on
```

# Authors
- Puru Tuladhar tuladharpuru@gmail.com
