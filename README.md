# Modul-5-Jarkom

I Putu Arya Prawira Wiwekananda-5025211065<br>
Hanifi Abrar Setiawan-5025211066<br>
Muhammad Fadhlan Asila Harashta-5025211068<br>

## Topologi
![Topologi](https://cdn.discordapp.com/attachments/903112010504482836/1185193704810623076/image.png?ex=658eb8a7&is=657c43a7&hm=0c436d98a611d38e011d1eaf582788c69a36b8d54e3abcbec92c7c5517772d97&)

## Tree VLSM
![Tree](https://cdn.discordapp.com/attachments/1173915504872796160/1185213790120329216/image.png?ex=658ecb5b&is=657c565b&hm=7315d2905115e3e056262ffe3c42644d6ed95aa6512827aa9d553bddfde75de4&)

## Prefix IP Route

| No | Subnet | Host | Netmask | Address | Network ID (NID) |
|---|--------|------|---------|---------|------------------ |
| 1 | A1     | 2    | /30     | 4       | 10.79.14.128      |
| 2 | A2     | 1023 | /21     | 2048    | 10.79.1.0         |
| 3 | A3     | 514  | /22     | 1024    | 10.79.8.0         |
| 4 | A4     | 2    | /30     | 4       | 10.79.132         |
| 5 | A5     | 2    | /30     | 4       | 10.79.14.136      |
| 6 | A6     | 2    | /30     | 4       | 10.79.14.140      |
| 7 | A7     | 257  | /23     | 512     | 10.79.12.0        |
| 8 | A8     | 66   | /25     | 128     | 10.79.14.0        |
| 9 | A9     | 2    | /30     | 4       | 10.79.14.144      |
|10 | A10    | 2    | /30     | 4       | 10.79.14.148      |

## Subneting

### Aura Configuration
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.79.14.129
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.79.14.133
	netmask 255.255.255.252
```

### Heiter Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.14.130
	netmask 255.255.255.252
        gateway 10.79.14.129

auto eth1
iface eth1 inet static
	address 10.79.1.1
	netmask 255.255.248.0

auto eth2
iface eth2 inet static
	address 10.79.8.1
	netmask 255.255.252.0
```

### Turk Region Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.1.2
	netmask 255.255.248.0
        gateway 10.79.1.1
```

### Frieren Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.14.134
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.79.14.137
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.79.14.141
	netmask 255.255.255.252
```

### Sein Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.8.2
	netmask 255.255.252.0
        gateway 10.79.8.1
```

### Grobe Forest Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.8.3
	netmask 255.255.252.0
        gateway 10.79.8.1
```

### Stark Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.14.138
	netmask 255.255.255.252
        gateway 10.79.14.137
```

### Himmel Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.14.142
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.79.12.1
	netmask 255.255.255.252

auto eth2
```

### Laub Hills Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.12.2
	netmask 255.255.255.252
        gateway 10.79.12.1
```

### Fern Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.14.3
	netmask 255.255.255.128

auto eth1
iface eth1 inet static
	address 10.79.14.145
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.79.14.149
	netmask 255.255.255.252

```

### Richter Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.14.146
	netmask 255.255.255.252
        gateway 10.79.14.145
```

### Revolte Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.14.150
	netmask 255.255.255.252
        gateway 10.79.14.149
```

### Schewer Mountain Configuration
```
auto eth0
iface eth0 inet static
	address 10.79.14.2
	netmask 255.255.255.128
        gateway 10.79.14.1
```
