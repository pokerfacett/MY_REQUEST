# Repository
https://github.com/espressif

# Package
https://github.com/espressif/esp-idf

# Impact
Esp-idf BLE_MESH module, when processing new devices joining the mesh network, there is a buffer overflow when parsing BLE broadcast packets. The specific location is in the bt_mesh_proxy_client_adv_ind_recv function of proxy_client.c. An attacker could construct ble packets to cause denial of service or remote code execution of device

# Affect Versions
4.0、4.0.1、3.3.2、3.3.1、3.3

# Patched Versions
4.2、4.1、3.3

# Patches
Issue has been patched in version 4.2、4.1、3.3 by check the length of net_id as follow:

`
if (buf->len != sizeof(ctx.net_id.net_id)) {
            BT_WARN("Malformed Network ID");
            return;
}
`

# Workarounds
https://github.com/espressif/esp-idf/commit/fab9b944a47067024ac61e48a08945e02b924369 And upgrade the sdk to 3.3、4.1、4.2

# For more information
If you have any questions or comments about this advisory:
Email us at qulewei@baidu.com

# Acknowledgements
repoter :qulewei

# References
https://github.com/espressif/esp-idf/issues/5035
https://github.com/espressif/esp-idf/commit/fab9b944a47067024ac61e48a08945e02b924369
