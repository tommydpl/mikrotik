# Mikrotik scripts

## add-tagged-vlan
`add-tagged-vlan.txt` - add vlans to mikrotik switch

**Assumptions:**
* more or less default confiuration
* one briddge named `bridge`

### Usage example: 

```
[admin@switch] > :global iflist "ether3,ether4,ether5"
[admin@switch] > :global vlanlist "150,151,152,153,154,155"
[admin@switch] > /system/script/run add-tagged-vlan 
set tagged interfaces for vlan 150 to bonding1;bonding2;ether3;ether4;ether5
set tagged interfaces for vlan 151 to bonding1;bonding2;ether3;ether4;ether5
set tagged interfaces for vlan 152 to bonding1;bonding2;ether3;ether4;ether5
add 153 to interfaces ether3,ether4,ether5
add 154 to interfaces ether3,ether4,ether5
add 155 to interfaces ether3,ether4,ether5
```
