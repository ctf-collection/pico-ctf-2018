# HEEEEEEERE'S Johnny!
Okay, so we found some important looking files on a linux computer. Maybe they can be used to get a password to the process. Connect with nc 2018shell.picoctf.com 35225. Files can be found here: passwd, shadow

# Solution
1. sudo apt install hashcat
2. create a file hash.txt that contains the hash. `$6$HRMJoyGA$26FIgg6CU0bGUOfqFB0Qo9AE2LRZxG8N3H.3BK8t49wGlYbkFbxVFtGOZqVIq3qQ6k0oetDbn2aVzdhuVQ6US.`.
3. hashcat -m 1800 -a 0 -o cracked.txt --remove hash.txt rockyou.txt --force
4. cracked.txt contains the password found. `$6$HRMJoyGA$26FIgg6CU0bGUOfqFB0Qo9AE2LRZxG8N3H.3BK8t49wGlYbkFbxVFtGOZqVIq3qQ6k0oetDbn2aVzdhuVQ6US.:hellokitty`.
5. the username is `root`, the password is `hellokitty`.