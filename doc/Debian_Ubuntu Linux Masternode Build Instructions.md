
# Debian/Ubuntu Linux Masternode Build Instructions: 
===================================================

Before this you need runing headless daemon in linux, you can make following this instructions: https://github.com/Hser2bio/SPE#debianubuntu-linux-daemon-build-instructions

In windows wallet go to console and type: 
```
getnewaddress MN1
```
take this address and send exact 1000 SPEs, when is confirmed atleast with 1 confirmations, type in console:
```
masternode genkey 
masternode outputs
```
take note of this info in txt, later we will need. 

In linux, stop daemon:
```
./MyTicketCoin-cli stop
```
now we need modify daemon conf:
```
cd .MyTicketCoin
nano MyTicketCoin.conf
```
need add this info in your MyTicketCoin.conf
```
rpcuser=xxxx
rpcpassword=xxxx
rpcallowip=127.0.0.1
listen=1
server=1
daemon=1
logintimestamps=1
maxconnections=256
masternode=1
externalip=yourvpsIP:34441
masternodeprivkey=xxxxxxxxxxxxxxxxx (that you get in windows console)
```
now we come back to windows wallet, go to tools, and open masternode conf file and add:
```
MN1 IP:PORT masternodekey masternodeouputs txnumber
EXAMPLE: 38.25.122.251:34441 7NEGGttKZojkAzViEYXXXxKTFdAtC2uSiMg8NSFqYVBtN6mYdU 7a1ebb4baadf9ff39bbbfc2d58fd57ff15b65a5096069c8XXX3fb4cb5c 1
```
save masternode conf file reopen wallet and in masternode section type START ALL

need atleast 22 blocks to be confirmed and start to work



