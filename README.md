# wifi-cli
A command-line tool for managing Wi-Fi in macOS

```
usage: wifi-cli [-h] [-v] [-i INTERFACE]
                {history,preferred,showpass,scan,join,disconnect,status,info,mac,power}
                ...

A command-line tool for managing Wi-Fi in macOS

positional arguments:
  {history,preferred,showpass,scan,join,disconnect,status,info,mac,power}
                        available commands
    history             list joined wireless networks history
    preferred           list preferred wireless networks
    showpass            show wireless network password stored in keychain
    scan                scan for wireless networks
    join                join a wireless network
    disconnect          disconnect from a wireless network (requires root)
    status              show currently connected wireless network
    info                show info about currently connected wireless network
    mac                 show Wi-Fi device hardware (MAC) address
    power               control Wi-Fi device power state

optional arguments:
  -h, --help            show this help message and exit
  -v, --version         show program's version number and exit
  -i INTERFACE          If an interface is not specified, wifi-cli will use
                        the first Wi-Fi interface on the system.
```

## Install
```
curl -sO https://raw.githubusercontent.com/tuladhar/wifi-cli/master/wifi-cli
install -m 755 wifi-cli /usr/local/bin
```
OR
```
git clone https://github.com/tuladhar/wifi-cli
cd wifi-cli
install -m 755 wifi-cli /usr/local/bin
```

## Scan for wireless networks
```
$ wifi-cli scan
```

## List joined wireless networks history
```
$ wifi-cli history
```

## Join an open wireless network
```
$ wifi-cli join -h
usage: wifi-cli join [-h] network password

positional arguments:
  network     network name
  password    network password

optional arguments:
  -h, --help  show this help message and exit
```

```
$ wifi-cli join "insecure-network" ""
```

## Join a protected wireless network
```
$ wifi-cli join "protected-network" "secret-password"
```

## Disconnect from a wireless network (requires root)
```
$ sudo wifi-cli disconnect
```

## Control Wi-Fi Power
```
$ wifi-cli power status
Wi-Fi device en1 is currently powered on
```

```
$ wifi-cli power off
Wi-Fi device en1 powered off
```

```
$ wifi-cli power on
Wi-Fi device en1 powered on
```

# Authors
* Puru Tuladhar
