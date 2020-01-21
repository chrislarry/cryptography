# cryptography
Cryptography is a method of protecting information and communications through the use of codes so that only those for whom the information is intended can read and process it. The pre-fix "crypt" means "hidden" or "vault" and the suffix "graphy" stands for "writing."



random-md5-generator creating a random password with md5sum encrypt it and then save the encrypted password in md5keys.txt
# how to use 
./random-md5-generator

292425650
41c16939b4f1a957f4fb773663aa5181  -
# delete the  - from the file md5keys.txt

# crack with
# hashcat -m 0 -a 3  md5keys.txt ?d?d?d?d?d?d?d?d


# then use 
# hashcat -m 0 -a 3  md5keys.txt ?d?d?d?d?d?d?d?d --show 
