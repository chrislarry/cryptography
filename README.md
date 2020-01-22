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
