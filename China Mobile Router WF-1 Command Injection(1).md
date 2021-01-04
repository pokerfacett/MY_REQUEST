# Background
China Mobile WF-1 router is an AX1800 router based on Qualcomm's five-core processor. It adopts a new generation of 11AX technology, 2.4G and 5G dual-band concurrently, and can provide a wireless rate of 1800M, providing high-speed and stable WiFi coverage

# Description
China Mobile Router WF-1 provide web interface /api/ZRQos/set_online_client which receive parameters by POST request, and the parameter ip field has a command injection vulnerability, An attacker can use the vulnerability to execute remote commands

# Affect Versions
V1.0.1

# POC
![image](https://github.com/pokerfacett/MY_REQUEST/blob/master/ZQos%20RCE.png)

problem code is in zrQos.lua which receive params from http request as follow：

![image](https://github.com/pokerfacett/MY_REQUEST/blob/master/set_online_client1.png)

And param ip  not filtered and directly spliced into the command line parameters, causing command injection

![image](https://github.com/pokerfacett/MY_REQUEST/blob/master/set_online_client.jpg)

result of POC is：

![image](https://github.com/pokerfacett/MY_REQUEST/blob/master/result_command_injection1.png)

# Acknowledgements
repoter :Lewei Qu(曲乐炜) and Dongxiang Ke(柯懂湘)

# References
https://www.zhipinmall.com/prodetail?id=1266#skuId=3020

http://iot.10086.cn/
