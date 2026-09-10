## Decimal to binary (T1)
- 10 = 00001010
- 210 = 11010010
- 168 = 10101000
- 16 = 0000100
- 255 = 11111111
- 128 = 10000000
- 192 = 11000000
- 248 = 11111000
- 0 = 00000000

---
- To get these results, I took a number and divided it by 2 each time till it turns into 0. Depending on the number I got, I wrote down 0 (if the number was even) or 1 (if the number was odd). Then I’ll simply mirror the final result I’ve got.
- For example, 10. 10 is even so I wrote 0, then 10/2=5, 5 is odd so I wrote 1 and so on till 0, and 0 is odd so I write 1. I have got this result: 0101. Next, I simply add zeros until the number has eight digits (01010000). Then I simply reverse the number, and here is the result: 00001010.

## Binary to decimal (T1)
- 11000000 = 192
- 11111111 = 255
- 10101000 = 168
- 00010000 = 16
- 11111000 = 248
- 11010010 = 210

---
- To get this results, I multiplied each digit of the eight-digit number by 2 raised to the power of its position from right to left. I then added up all the numbers I've got and obtained the final result.
- For example 11111111. I take 1 from the right and multiply it by 2^0. Then I go through right to left: 1x2^1; 1x2^2; 1x2^3... I've got 1+2+4+8+16+32+64+128=255.

## Full-address conversion (T1)
- 10.210.168.16 = 00001010.11010010.10101000.00010000
- 192.168.0.1 = 11000000.10101000.00000000.00000001
- 172.16.5.100 = 10101100.00010000.00000101.01100100

- 11000000.10101000.00000001.00000001 = 192.168.1.1
- 00001010.00001010.00000000.01001011 = 10.10.0.75

---
## What class is it? (T2)
| Address | Class | Default Mask (dotted) | Default Mask (CIDR) |
| :--- | :--- | :---: | :--- |
| 10.0.0.5 | A | 255.0.0.0 | /8 |
| 192.168.1.1 | C | 255.255.255.0 | /24 |
| 172.16.4.20 | B | 255.255.0.0 | /16 |
| 8.8.8.8 | A | 255.0.0.0 | /8 |
| 200.100.50.25 | C | 255.255.255.0 | /24 |

## Mask ↔ CIDR ↔ binary (T2)
| Dotted-decimal | CIDR | Binary (32 bits, dots between octets) |
| --- | --- | --- |
| 255.255.255.0 | /24 |	11111111.11111111.11111111.00000000 |
| 255.255.0.0 | /16 | 11111111.11111111.00000000.00000000 |
| 255.0.0.0 | /8 | 11111111.00000000.00000000.00000000 |
| 255.255.255.192 | /26 | 11111111.11111111.11111111.11000000 |
| 255.255.248.0 | /21 | 11111111.11111111.11111000.00000000 |
| 255.255.255.128 | /25 | 11111111.11111111.11111111.1000000 |

- (The CIDR is determined by the sum of the values in the binary code)

## Networks and hosts per class (T2)
| Class | Default CIDR | Number of possible networks | Number of hosts per networks |
| --- | --- | --- | --- |  
| A | /8 | 128 nets | 16 million hosts |
| B | /16 | 16 000 nets | 65 000 hosts |
| C | /24 | 2 000 000 nets | 254 hosts |

## The five key values - the main event (T3)

### 172.16.0.0/16
- subnet mask:     255.255.0.0  
- network address:   172.16.0.0
- default gateway:   172.16.0.1
- host range start:  172.16.0.1
- host range end:    172.16.0.254
- broadcast:         172.16.255.255
### 10.10.0.0/26
- subnet mask:       255.255.255.192
- network address:   10.10.0.0
- default gateway:   10.10.0.1
- host range start:  10.10.0.1
- host range end:    10.10.0.62
- broadcast:         10.10.0.63
- ((32 – 26 = 6). Maximum bits for last octet is 64 (2^6 = 64))
### 192.168.5.0/28
- subnet mask:     255.255.255.240
- network address:   192.168.5.0
- default gateway:   192.168.5.1
- host range start:  192.168.5.1
- host range end:    192.168.5.14
- broadcast:         192.168.5.15
- ((32 – 28 = 4). Maximum bits for last octet is 64 (2^4 = 16))
### 10.0.0.0/30
- subnet mask:     255.255.255.252
- network address:   10.0.0.0
- default gateway:   10.0.0.1
- host range start:  10.0.0.1
- host range end:    10.0.0.2
- broadcast:         10.0.0.3
### 192.168.100.128/25
- subnet mask:     255.255.255.128
- network address:   192.168.100.128
- default gateway:   192.168.100.129
- host range start:  192.168.100.129
- host range end:    192.168.100.254
- broadcast:         192.168.100.255
- (The /25 divides the network into two subnets of 128 each)

---
## Which subnet does this host belong to? (T4)
### 10.10.0.75/26
- Network address of this subnet: 10.10.0.64
- Broadcast of this subnet: 10.10.0.127
- This is a host address. Since the number 75 falls within the range between 65 and 126, this address can be assigned to a specific device
### 192.168.1.200/26
- Network address of this subnet: 192.168.1.192
- Broadcast of this subnet: 192.168.1.254
- This is a host. This address belongs to the fourth subnet (according to /26 mask), where the range of the last octet (200) is from 192 to 255.
### 172.16.5.130/25
- Network address of this subnet: 172.16.5.128
- Broadcast of this subnet: 172.16.5.255
- This is a host. This address belongs to second subnet (according to /25 mask), where the range of the last octet is from 128 to 255.
### 10.0.0.0/30
- Network address of this subnet: 10.0.0.0
- Broadcast of this subnet: 10.0.0.3
- This is a host address. Mask /30 leaves only 2 bits for the host. The subnet mask is 4. For this reason, the IP address space is divided into very small blocks of 4 addresses each. Find a divisor (4), the nearest number that is divisible by 4 without a remainder is 0 so network address is 10.0.0.0. And broadcast is 4-1=3.
