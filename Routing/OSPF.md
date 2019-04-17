# OSPF

1. [Router ID](#router-id)
1. [Hello Packets](#hello-packets)

## Router ID

* 32 Bit, like ipv4 address even for OSPFv3
* 0.0.0.0 Is Reserved
* Multiple Processes need unique ID, even VRF

### Precedence of assignment
1. Manual Configuration
2. Highest IPv4 on loopback interface
    * **Can't be Admin Down**
3. Highest IPv4 on non-loopback interface
    * Can be down/down
    * **Can't be Admin Down**

## Packet Types


### Hello
* RFC 2328
* Dead Interval is 4 times Hello Interval by default
* Wait Interval = Dead Interval
* TTL = 1
* Multicast 224.0.0.5 (IPv4): FF02::5 (IPv6) on Broadcast Network
* L2 Destination 0100.5e00.0005
* Destination is unicast on non-broadcast networks
* If 'point' is in name, no DR/BDR election
* Subnet mask is only check on broadcast media links

### Databse Description (DBD)
### Link-State Request (LSR)
### Link-State Update (LSU)
### Link-State Acknowledgement (LSAck)


## Misc Notes
* Designated Router: TBD
* Backup Designated Router: TBD
* Protocol: OSPF IGP (89)


## Commands
* `RT(config)# router ospf <process id>` 
* `RT# show ip ospf neighbors`
* `RT# show ip ospf interface <interface>`
