# Repository
https://github.com/espressif

# Package
https://github.com/espressif/esp-idf

# Impact
In the process of BluFi's network configurationg through ble, there is an overflow when processing the write ATT command at characteristic = 0xFF01. The specific problem is in the btc_blufi_recv_handler function of blufi_prf.c. First ,parse the incoming ATT data data [0] and data [1] as the length of memery which apply from heap. And then copy the memory data starting from data [2] to the applyed memory, causing a buffer overflow

# Affect Versions
all versions the latest version is 4.2

# Patched Versions
NULL

# Patches


# Workarounds
NULL

# For more information
If you have any questions or comments about this advisory:
Email us at weixiaocikett@gmail.com

# Acknowledgements
repoter :qulewei

# References
https://github.com/espressif/esp-idf/issues/5048

