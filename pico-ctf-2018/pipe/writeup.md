# Pipe
During your adventure, you will likely encounter a situation where you need to process data that you receive over the network rather than through a file. Can you find a way to save the output from this program and search for the flag? Connect with 2018shell.picoctf.com 2015.

# Writeup
1. touch out.txt
2. nc 2018shell.picoctf.com 2015 > out.txt
3. ^C
4. find `pico*` in out.txt