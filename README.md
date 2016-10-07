# A2osX
Multi-Tasking OS for Apple II
## Requires :
Enhanced IIe (65c02 cpu) with 128k, //c, IIgs

## General Information:  
**A2OSX.BOOT.po** : 140k A2osX boot disk with all binaries  
**A2OSX.DEV.po**  : 140k A2osX disk with ASM binaries & INClude files  
**A2OSX.SRC.po**  : 800k S-C MASM boot disk with all sources  
  
OApple+1,OApple+2,OApple+3 to switch between screens : Kernel Log, text, DHGR.  
(OApple+shift+1,OApple+shift+2,OApple+shift+3 on FR keyboard)  
  
### **** Developers WANTED ****  

!!! Help on writing this code should be greatly appreciated !!!  

...
In Progress : moving TCPIP to socket API
In Progress : moving KERNEL to AuxLC Bnk1 & 2 (16k, more space for drivers)
...

## SYS/KM* Supported Hardware At Kernel Level (ProDOS):
| KM.Name | Status | Comment |
| ------- | ------ | ------- |
| KM.NSC | Working | No-Slot-Clock |
| KM.RAMWORKS | Working | AE-Ramworks I,II,III |
  
## SBIN,Daemons/Commands:  
| Name | Status | Comment | K.Ver |
| ---- | ------ | ------- | ----- |
| INSDRV | Working | |
| GETTY | Working | |
| LOGIN | In Progress | no auth using /etc/passd yet |
| TCPIP | In Progress | New Socket API. ARP,IP,ICMP,UDP ok, TCP in progress |
| DHCPCLNT | Working | rewritten to use new Socket API |
| SHELL | Working | (See Internal Shell commands) |
  
## DRV,Drivers:  
| Name | Status | Comment | K.Ver |
| ---- | ------ | ------- | ----- |
| Console.DRV | Working | ANSI support in Progress. |
| PIC.DRV | In Progress | Apple "Parallel Interface Card" Driver, renamed from PPIC.DRV|
| SSC.DRV | In Progress | |
| SSC.I.DRV | In Progress | |
| Mouse.DRV | Working | |
| Uthernet.DRV | Working | |
| Uthernet2.DRV | Working | |
| Uther2.AI.DRV | In Progress | With ARP/IP Offloading |
| LanCeGS.DRV | Working | |
| Mouse.DRV | Working | |
| DHGR.DRV | In Progress | except bitblt... |
  
## Internal Shell commands:  
| Name | Status | Comment | K.Ver |
| ---- | ------ | ------- | ----- |
| CD | Working | |
| DATE | Working  | |
| ECHO | Working | |
| EXIT | Working  | |
| IF | | |
| PAUSE | Working | |
| READ | | |
| TIME | Working | |
| TYPE | Working | |
| SET | Working  | |
| STARTPROC | Working  | Used in A2osX.startup |
  
## BIN,External Shell commands:  
| Name | Status | Comment | K.Ver |
| ---- | ------ | ------- | ----- |
| MEM | Working | | |
| LSDEV | Working | | |
| PS | Working | | |
| MD | Working | | |
| RM | Working | switches not yet implemented, new ArgC/Arg[] coming... | |
| LS | Working  | BUG: `ls dir` does not list dir content (`ls dir/` works) | |
| CP | Working| switches not yet implemented, new ArgC/Arg[] coming...  | |
| ARP | Working | dump ARP cache, setup a static ARP entry | |
| PING | Working | | |
| DNSINFO | Working | dump DNS cache, setup a static DNS entry | |
| IPCONFIG | Working | renamed from NETINFO | |
| NETSTAT | Working | | |
| RPCDUMP | Working | tool based on UDP socket API, renamed from RPCINFO | |
| EDIT | Working | still missing : find/replace | |
| NSCUTIL | Working | Tool for setting time in NSC/DL1216E | |
| ASM | In Progress | S-C MASM based multi CPU assembler | |
  
## Misc  
### S-C MASM color scheme for Notepad++  
...drop _Tools/userDefineLang.xml in %APPDATA%\Notepad++  
;-)

