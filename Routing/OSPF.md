# OSPF

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