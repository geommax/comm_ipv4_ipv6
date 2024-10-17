# comm_ipv4_ipv6
network comm_ipv4_ipv6

HB
TB
GB   1 G
MB.  1024  MB
KB. 
Byte
Bit 


1024 KB >    1 MB
1024 Byte > 1 KB

1 Byte >  8  Bits


IPv4 address is a 32-bit n u m ber

32 bits >. 4 Bytes


1. Calculating the network address for 192.168.1.107/24:
* Host Address: 192.168.1.107
    * Binary representation: 11000000.10101000.00000001.01101011
* Network Prefix: /24 or 255.255.255.0
    * Binary representation of the subnet mask: 11111111.11111111.11111111.00000000
    * The first 24 bits are for the network, and the last 8 bits are for the host.
* Network Address: The network address is obtained by doing a bitwise AND operation between the host address and the subnet mask. This clears the host part of the IP, leaving the network part.


Network Address ကိုတွက်ထားတာ 

11000000.10101000.00000001.01101011            << Host address
11111111.	   11111111.     11111111.   00000000.      << Subnet Mask 
===-=-=-=- BIT WISE AND =-=-=-=====
11000000.10101000.00000001.00000000		<< Network Address. 
Conver to decimal (Network address 192.168.1.0 ) 24

<< router address (192.168.1.1) . 

Host အရေအတွက် ဘယ်နှခုချိတ်လို့ရမလဲ ?

2^8 ‎ = 256. 

192.168.1.1, 192.168.1.254. 

Phone တစ်လုံးအတွက် (192.168.1.2) , computer (192.168.1.3), cctv (192.168.1.4)

(192.168.1.255) 255 သည် broast address ဖစ်သွားတဲ့အတွက်ပါ။

    * 
    * Binary: 11000000.10101000.00000001.00000000
    * Result: 192.168.1.0
* Broadcast Address: The broadcast address is obtained by setting all the host bits to 1.
    * Binary: 11000000.10101000.00000001.11111111
		
00000001
Broadcast Address တွက်ထားတာ
			
11111111
2^7 + 2^6 + 2^5 +2^4+ 2^3 + 2^2 + 2^1 + 2^0

128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 ‎ = 255

    * Result: 192.168.1.255

11000000.10101000.00000001.00000000	
00000000.00000000.00000000.11111111
=====-=-==- Bitwise OR =-=-=-=-=-====
 11000000.10101000.00000001.11111111

2. Calculating the network address for 10.1.1.18/8:
* Host Address: 10.1.1.18
    * Binary representation: 00001010.00000001.00000001.00010010
* Network Prefix: /8 or 255.0.0.0
    * Binary representation of the subnet mask: 11111111.00000000.00000000.00000000
    * The first 8 bits are for the network, and the remaining 24 bits are for the host.
* Network Address: Do a bitwise AND between the host address and the subnet mask:
    * Binary: 00001010.00000000.00000000.00000000

	00001010  =   10
2^7 + 2^6 + 2^5 +2^4+ 2^3 + 2^2 + 2^1 + 2^0
0+0+0+0 + 8 + 0 + 2 + 0 ‎ = 10

       00000000 =   0

    * Result: 10.0.0.0
						2^8*2^8 * 2^8 ‎ = 16,777,216


			24.0.0.0 
2^8*2^8 * 2^8 ‎ = 16,777,216


* Broadcast Address: Set all the host bits to 1.
					00001010.00000000.00000000.00000000  << network address
					00000000.11111111.11111111.11111111			<< ကွကိုယ်သတ်မှတ်ထာ
					====-=-=- BITWISE OR =-=-=-====
    * Binary: 00001010.11111111.11111111.11111111 
					
    * Result: 10.255.255.255


Host အရေအတွက် ဘယ်နှခုချိတ်လို့ရမလဲ ?
Network Address ထုတ်ဖော်ပါ။ တွက်ထုတ်ပုံ။
Broadcast address ဘယ်လောက်လဲ?  ထွက်ထုတ်ပုံ။ 	



3. Calculating the network address for 172.16.181.23/19:
* Host Address: 172.16.181.23
    * Binary representation: 10101100.10101000.10110101.00010111
* Network Prefix: /19 or 255.255.224.0
    * Binary representation of the subnet mask: 11111111.11111111.11100000.00000000
    * The first 19 bits are for the network, and the remaining 13 bits are for the host.
* Network Address: Perform a bitwise AND between the host address and the subnet mask:
    * Binary: 10101100.10101000.10100000.00000000
    * Result: 172.168.160.0
* Broadcast Address: Set all the host bits to 1.
    * Binary: 10101100.10101000.10111111.11111111
    * Result: 172.168.191.255
General Steps for Calculating Network and Broadcast Addresses:
1. Convert the host IP address into binary.
2. Convert the network prefix (subnet mask) into binary.
3. To find the network address:
    * Perform a bitwise AND between the host address and the subnet mask.
4. To find the broadcast address:
    * Take the network address and set all the host bits (determined by the prefix length) to 1.
 
