### Warmup
Reversing
> Here's a quick rev challenge to get started. Reverse the binary to obtain the flag.
> The flag format is shellctf{...}


Ghidra

first lines of main function, could be our flag

![[Pasted image 20220812184208.png]]

![[Pasted image 20220812184426.png]] 
Nope :-(

renamed some variables
![[Pasted image 20220812184858.png]]

flag length should be 27
![[Pasted image 20220812184946.png]]



![[Pasted image 20220812185233.png]]

each element of our possible flag is bitshifted before compared to our input

![[Pasted image 20220812185512.png]]
That's it!

```
>>> flag = [0x1cc,0x1a0,0x194,0x1b0,0x1b0,0x18c,0x1d0,0x198,0x1ec,0x188,0xc4,0x1d0,0x15c,0x1a4,0xd4,0x194,0x17c,0xc0,0x1c0,0xcc,0x1c8,0x104,0x1d0,0xc0,0x1c8,0x14c,500]
>>> final_flag = ""
>>> for hex_num in flag:
...     final_flag += chr(hex_num >> 2)
... 
>>> final_flag
'shellctf{b1tWi5e_0p3rAt0rS}'

```
