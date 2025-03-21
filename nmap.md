# Description
This file lists everything you need to know to use ```nmap``` well as a beginner!

### Commands in terminal
- ```nmap <host-ip-address>```: scan IP address for open ports
- ```-sV```: show service version of open ports
- ```-sC```: run default scripts, provides additional details to ```-sV```
- ```-p-```: scan all ports (1-65535) instead of only 1000 most common ports. very slow, recommend use with ```-T5``` (see below)
- ```-T1``` to ```-T5```: speed of sending packages, from slowest to fastest. ```-T1``` is hard to detect, while ```-T5``` is very easily detected
