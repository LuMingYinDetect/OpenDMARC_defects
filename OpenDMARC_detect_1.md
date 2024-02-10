Affected Version:
OpenDMARC 1.4.2 9cebf724d601452d1a671ed5331551dbc18df83a

Vulnerability Description:
This is a null pointer dereference vulnerability occurring at line 1480 in the file /OpenDMARC/libopendmarc/opendmarc_policy.c. This vulnerability could be exploited maliciously, leading to program crashes and denial-of-service incidents.

OpenDMARC download address:
https://github.com/trusteddomainproject/OpenDMARC.git

Vulnerability details:
1.When list_buf is NULL in the if condition at line 1478 of the file /OpenDMARC/libopendmarc/opendmarc_policy.c and size_of_buf > 0, the if statement will enter the true branch. This leads to a null pointer dereference vulnerability at line 1480, where the first argument of the memset function is list_buf, which is NULL. Consequently, this results in a program crash, as illustrated in the following image:

![image](https://github.com/LuMingYinDetect/OpenDMARC_defects/blob/main/OpenDMARC_1.png)
