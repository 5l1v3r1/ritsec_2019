# CSC Major 2019
Cyber Skills Challenge - Major - 2019

## Overview

**URL:** https://ctf.fifthdomain.com.au (site will remain online)  
**Organisors:** ADF Cyber Skills Challenge 
**Duration:** ? days  
**Team mates:** Individual Competition  

```
Title                         Category        Points  Flag
----------------------------- --------------- ------- ---------------------------------------
URGGGGGG                        Forensics       480    RITSEC{wH0_s@id_n3twork1nG_wAs_tH3_oNlY_pAck3t_TyP3}
Our First API                   Web             417    RITSEC{JWT_th1s_0ne_d0wn}


```
---
## URGGGGGG

* **Category:** Forensics
* **Points:** 480

### Challenge

> One of our operatives sent us this packet capture but we aren't quite sure what to make of it, what can you find?

[URGGGGGG.pcapng](/writeupfiles/URGGGGGG.pcapng)

### Solution

> tshark -r URGGGGGG.pcapng -Y "((usb.transfer_type == 0x01) && (frame.len == 35)) && !(usb.capdata == 00:00:00:00:00:00:00:00)" -e "usb.capdata" -Tfields | sed 's/://g' > URGGGGGG.txt

[map_keystroketool.py](/writeupfiles/map_keystroketool.py)

> python map_keystroketool.py > URGGGGGG_solve.txt

> Now look for the RITSEC{} flag pattern and try to make out the keystrokes, paying attention to SHIFT, CTRL-x, CTRL-c, CTRL-v keys used. You can guess the letters that has been copied/cut and pasted.

[URGGGGGG_solve.txt](/writeupfiles/URGGGGGG_solve.txt)


**Flag**
```
RITSEC{wH0_s@id_n3twork1nG_wAs_tH3_oNlY_pAck3t_TyP3}
```
---
## Our First API

* **Category:** Web
* **Points:** 417

### Challenge

> ctfchallenges.ritsec.club:3000 ctfchallenges.ritsec.club:4000

Hint: You don't need the Bearer keyword!

### Solution

> jwt_tool.py

**Flag**
```
RITSEC{JWT_th1s_0ne_d0wn}
```
---


## ?

* **Category:** Misc
* **Points:** 100

### Challenge

> 

[peek-a-boo.pcap](/writeupfiles/peek-a-boo.pcap)

### Solution

> ?

**Flag**
```
flag{}
```
---
