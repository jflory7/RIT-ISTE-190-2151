# ISTE-190 - Network Address Translation

## Problem
* We need more IP addresses
* In beginning: Few foresaw the growth of the Internet
 * Only 32-bits were deemed necessary for network and host addressing
 * As it turned out, IPv4 32-bit address space too small
 * 4.29 billion potential addresses is too small

## Solution: Private IP networks
* Two types of IP networks
 * Public
 * Private (if you have a (home) router, you have private, local area network)
* Two types of IP addresses
 * Public: Accessible over the public Internet
 * Private: Only accessed within a private local area network (LAN)

## Private IP addresses
* Assigned by DHCP from the home router
* By convention, private networks use one of three private IP address ranges
 * Addresses that begin with: 192.168.xx.xx, 10.xx.xx.xx, 172.xx.xx.xx

## Network Address Translation (NAT)
* Strategy to deal with address space problem is to use private IP addresses at the LAN level
 * Only need to be unique within the LAN
* NAT automatically translates between public <=> private addresses
* Since routers connect networks, they have two public IP addresses, one for each network connected to router
* NAT router also has two addresses:
 * Public address interfacing with the Internet
 * Private address interfacing with the LAN

## Client-Server Model
* Each packet will have from (source) IP address and a to (destination) IP address
* Client-server model consists of:
 * Port number: Random number generated by the OS in the range of 1025-65536
 * Port number is appended to the from IP address using a colon (e.g. 123.45.678.90:25565)
 * Socket is combination of an IP address and a port number
 * Server uses socket to send data back to the client
* Well-known ports
 * Pre-assigned by the Internet Assigned Number Authority (IANA)
* Examples of well-known ports:
 * 53 DNS (Domain Name System)
 * 80 HTTP (Web)
 * 110 POP (Post Office Protocol; retrieve email from mail server)
 * 443 HTTPS (Secure HTTP)
 * 546 DHCP (Dynamic Host Configuration Protocol)
* Well-known ports also appended to the IP address

## NAT architecture
![NAT architecture graphic](https://i.j-f.co/u/39d46e600dd1ffdd1c960de165164e27.png)