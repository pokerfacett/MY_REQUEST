# Repository
https://www.realtek.com/en/component/zoo/category/rtl8723de-software

# Package
https://www.realtek.com/en/component/zoo/category/rtl8723de-software


# Impact
When realtek BLE protocol stack handles the device connection message CONNECT_REQ, the Interval field is not handled properly, and the attacker can launch a denial of service attack remotely

# Affect Versions
<=4.1

# Patched Versions
NULL

# POC

# Prove
`
Link Layer Data
  Access Address: 0x9a328370
  CRC Init: 0x179a9c
  Window Size: 2 (2.5 msec)
  Window Offset: 2 (2.5 msec)
  Interval: 0 (0 msec)
  Latency: 0
  Timeout: 50 (62.5 msec)
`

dmesg.log
`
[  584.475344] Bluetooth: Peer acked invalid packet
[  584.480585] Bluetooth: Peer acked invalid packet
[  584.501450] Bluetooth: Peer acked invalid packet
[  584.533039] Bluetooth: Peer acked invalid packet
[  584.564637] Bluetooth: Peer acked invalid packet
[  584.596220] Bluetooth: Peer acked invalid packet
[  584.627825] Bluetooth: Peer acked invalid packet
[  584.659400] Bluetooth: Peer acked invalid packet
[  584.690988] Bluetooth: Peer acked invalid packet
[  584.721535] Bluetooth: hu c6761cc0 retransmitting 2 pkts
[  584.722592] Bluetooth: Peer acked invalid packet
[  584.733497] Bluetooth: Peer acked invalid packet
[  584.739112] Bluetooth: Peer acked invalid packet
[  584.765247] Bluetooth: Peer acked invalid packet
[  584.796834] Bluetooth: Peer acked invalid packet
[  584.828433] Bluetooth: Peer acked invalid packet
[  584.860023] Bluetooth: Peer acked invalid packet
[  584.891611] Bluetooth: Peer acked invalid packet
[  584.923200] Bluetooth: Peer acked invalid packet
[  584.954778] Bluetooth: Peer acked invalid packet
[  584.986387] Bluetooth: Peer acked invalid packet
`


# Workarounds


# For more information
If you have any questions or comments about this advisory:
Email us at qulewei@baidu.com

# Acknowledgements
repoter :qulewei

# References

