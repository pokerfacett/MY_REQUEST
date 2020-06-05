# Repository
https://github.com/espressif

# Package
https://github.com/espressif/esp-idf

# Impact
In the process of ESP IDF and blufi passing through the ble distribution network, there is overflow when processing the att command with the characteristic of 0xff01. The specific problem is blufi_ BTC of PRF. C_ blufi_ recv_ In the handler function, apply for memory space by parsing the data data [0] and data [1] passed in ATT, and copy the memory data from data [2] to the applied memory, causing buffer overflow
Esp-idf，BluFi通过ble配网过程中，在特性为0xFF01在处理写入ATT命令时存在溢出，具体问题在blufi_prf.c的btc_blufi_recv_handler函数中，通过解析传入ATT数据data[0]和data[1]，申请内存空间，并将data[2]开始的内存数据拷贝到申请的内存中，造成缓冲区溢出

# Affect Versions
all versions the latest version is 4.2

# Patched Versions
NULL

# Patches


# Workarounds
NULL

# For more information
If you have any questions or comments about this advisory:
Email us at qulewei@baidu.com

# Acknowledgements
repoter :qulewei

# References
https://github.com/espressif/esp-idf/issues/5048

