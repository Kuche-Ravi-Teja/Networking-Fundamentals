## <u> What is IP Addressing? <u/>

An IP (Internet Protocol) Address is a unique numerical label assigned to every device connected to a computer network.

## <u> The Real-World Example <u/> 

Think of an IP address exactly like a complete physical home mailing address.

  - If someone wants to send you a letter, the postal service needs your specific country, city, street, and house number. Without it, the letter cannot be delivered.

  - Similarly, if a YouTube server wants to send video data to your phone, it needs your phone's exact IP address to deliver those data packets to the right screen.

## 1. Address Formats : IPv4 vs IPv6

There are two versions of IP addresses currently used on the internet.

IPv4 (Internet Protocol Version

  - Definition : The traditional addressing system that uses a 32-bit binary number, written as four decimal numbers separated by dots (called octets). Each octet ranges from 0 to 255.
  - The Catch : It can only provide about 4.3 billion unique addresses. Because the world now has tens of billions of connected smart devices, we have completely run out of new IPv4 addresses.
  - Example: 192.168.1.45
  
IPv6 (Internet Protocol Version)

  - Definition : The modern upgrade created to replace IPv4. It uses a 128-bit binary number, written in hexadecimal code (numbers 0-9 and letters a-f) separated by colons.
  - The Benefit : It provides $3.4 \times 10^{38}$ unique addresses (an undecillion) - more than enough to give every single grain of sand on the planet its own massive network.
  - Example: 2001:0db8:85a3:0000:0000:8a2e:0370:73342.

  
## 2. Network Types: 

Public vs. Private IP AddressesIP addresses are divided into two distinct logical zones to save space and ensure security.
  
Private IP Addresses

  - Definition : Internal addresses used inside a private local network (like your home Wi-Fi or a corporate office). They are completely invisible to the outside internet.
  - Example : When you connect your smartphone and your laptop to your home Wi-Fi router, the router might assign your phone 192.168.1.5 and your laptop 192.168.1.6.
  - Your neighbor's router can use the exact same addresses inside their own house without any conflict, because those addresses never leave the building.
  
Public IP Addresses
  
  - Definition : A globally unique address assigned to your network gateway (your router) by your Internet Service Provider (ISP). This is the address that faces the global internet.
  - Example : When your laptop tries to load a website, it sends data through your router. To the rest of the internet, your request looks like it is coming from a single public address, such as 49.37.12.155. It acts like the main lobby mailbox of a massive apartment building.


## 3. Subnetting (Dividing the Network)

Definition : Subnetting is the strategy of splitting a single, large network into smaller, isolated sub-networks (called subnets).

  - Example : Imagine you own a massive 100-story corporate building. If you don't build internal walls, the entire building is just one giant open room. If the HR department shouts a message, all 10,000 employees are forced to hear it (wasted bandwidth). Furthermore, anyone can walk up and read sensitive payroll files on anyone else's desk (security risk).

By subnetting, you build concrete walls to separate the floors :

  - Floor 1 (Subnet A) : Web-facing customer lobby.
  - Floor 2 (Subnet B) : Private backend accounting databases.
  
In cloud computing (like AWS or Google Cloud), you use subnets to keep your web application servers accessible to the public, while locking your database servers away in a private subnet where the outside internet cannot touch them.


## 4. CIDR Notation (Classless Inter-Domain Routing)

Definition : A compact method used to specify an IP address and its associated routing prefix (subnet mask). It uses a forward slash (/) followed by a number to dictate exactly how much of the address is locked for the Network identity versus how much is free for individual Host devices.

#### The /24 Notation (The Small Block)What it means : The first 24 bits of the 32-bit address are locked. Only the final 8 bits are left open to assign to your machines ($32 - 24 = 8$ bits).
  - Number of available spaces: $2^8 = 256$ total IP addresses.
  - Example: If a cloud engineer sets up a subnet with 10.0.1.0/24:The 10.0.1. part is completely locked like a street name.You can assign the final slot to individual computers, ranging from 10.0.1.1 to 10.0.1.254.
  
#### The /16 Notation (The Large Block)What it means : The first 16 bits are locked. The remaining 16 bits are completely wide open for you to use ($32 - 16 = 16$ bits).
  - Number of available spaces: $2^{16} = 65,536$ total IP addresses.
  - Example: When you create an overall Virtual Private Cloud (VPC) network, you might give it a massive block like 10.0.0.0/16. Because you have so many addresses available in this block, you can later carve it up into smaller /24 subnets (e.g., 10.0.1.0/24 for Web Servers, 10.0.2.0/24 for App Servers).
  
#### The /32 Notation (The Single Target)What it means : All 32 bits are locked ($32 - 32 = 0$ free bits).
  - Number of available spaces: Exactly 1 unique IP address.
  - Example: If you configure a cloud firewall rule to allow remote access to your database, you don't want to open it up to the whole world. You specify your exact, personal office IP address followed by /32 (e.g., 198.51.100.4/32). This tells the firewall to grant access to only your exact laptop and absolutely nobody else.
