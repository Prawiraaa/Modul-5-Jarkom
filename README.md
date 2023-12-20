# Modul-5-Jarkom

I Putu Arya Prawira Wiwekananda-5025211065<br>
Hanifi Abrar Setiawan-5025211066<br>
Muhammad Fadhlan Asila Harashta-5025211068<br>

## Topologi GNS
![Topologi](https://cdn.discordapp.com/attachments/903112010504482836/1185193704810623076/image.png?ex=658eb8a7&is=657c43a7&hm=0c436d98a611d38e011d1eaf582788c69a36b8d54e3abcbec92c7c5517772d97&)

## Tree VLSM
![Tree](https://cdn.discordapp.com/attachments/903112010504482836/1186673828718452807/image.png?ex=65941b20&is=6581a620&hm=0d285d942c3de4b7d159c07c53a0c0991f1256ad03730a9321174839f5f5e5ba&)
Pertama tentukan jumlah dari masing masing CIDR. Dalam kasus ini ada 6 node dengan CIDR /30. Untuk mempermudah buat 6 node /30. Untuk kemudian naik terus sampai kita menemukan CIDR kedua tertinggi dalam topologi, dalam kasus ini adalah /25. Pastikan ada node kosong untuk /25 kemudian lakukan step tadi hingga node terendah dicapai. <br>
Menentukan IP
Kemudian untuk menentukan IP pada node CIDR /20 memiliki 4096 total address. Dikarenakan akan dibagi menjadi 2, masing masing CIDR /21 akan memiliki 2048 address. Dan seterus nya akan dibagi 2. Untuk mempermudah 2048 akan dibagi dengan 256 dan hasilnya ditambahkan pada ip atasnya. Misal 10.79.1.0 /20, dikarenakan CIDR /20 memiliki 4096 total address. Karena itu maka node dibawahnya masing masing memiliki 2048 total address. Kemudian 2048 akan dibagi 256 yang hasilnya 8. Dari sana maka salah satu node akan memiliki ip 10.79.1.0 - 10.79.7.255 dan node satu lagi 10.79.8.0 sampai 10.79.14.255 <br>

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
### Ping node lain
![ping](https://cdn.discordapp.com/attachments/1173915504872796160/1186661992036053112/image.png?ex=6594101a&is=65819b1a&hm=f863c331a8ec251a68f7e246318e2fc1f7306587f9d41e2b9529af7a887db86d&)

## Topologi CPT
![TopologiCPT](https://cdn.discordapp.com/attachments/945123026410831952/1186869034747179038/image.png?ex=6594d0ec&is=65825bec&hm=cf9ff27b5220854344af59b1c018bb504a04c3913d752fcc452e84a267730585&)

### Subnetting
Menggunakan metode yang sama dengan GNS

### Routing

#### Aura
![AuraCPT](https://cdn.discordapp.com/attachments/945123026410831952/1186869900388597860/image.png?ex=6594d1bb&is=65825cbb&hm=288dcca714d2a17a23bb5045c7f86f92d2261e23f52105ea1456f3fcfec01c93&)

#### Heiter
![HeiterCPT](https://cdn.discordapp.com/attachments/945123026410831952/1186870778118013019/image.png?ex=6594d28c&is=65825d8c&hm=87d64ff3d4a96111682a09ced8706c5bb3698dd2021df5c976a756f857c446e0&)

#### Frieren
![FrierenCPT](https://cdn.discordapp.com/attachments/945123026410831952/1186870914860728340/image.png?ex=6594d2ad&is=65825dad&hm=44d65e060133c82f63c3310e224f616d68273097ac079c7247cf03d9eb7c254b&)

#### Himmel
![HimmelCPT](https://cdn.discordapp.com/attachments/945123026410831952/1186871024822784032/image.png?ex=6594d2c7&is=65825dc7&hm=a86399bc02e1a587ff4dac8ff95ea0c5597dc5b214c5c3a9feb5d6cfcca36626&)

#### Fern
![FernCPT](https://cdn.discordapp.com/attachments/945123026410831952/1186871143731314688/image.png?ex=6594d2e3&is=65825de3&hm=158d4b86bcf038ad529c7ae8c8d1b49473774dda19176cdfbd62c2e0eeef1687&)
