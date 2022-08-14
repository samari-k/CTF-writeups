# Warmup

Category: Reversing

> Here's a quick rev challenge to get started. Reverse the binary to obtain the flag.
> The flag format is shellctf{...}

---

I opened up the given executable in **Ghidra** and inspected the main function. The first lines looked like they could be our flag or at least could lead us to our flag. (On the screenshot next to the variables I wrote down the characters they were supposed to be to actually be the flag).

<img src="../screenshots/Pasted image 20220812184208.png" width=250>

I thought they mabe just a bit shifted by having added some value. But a quick python try said nope.

<img src="../screenshots/Pasted image 20220812184426.png" width=200> 

So I head a deeper look and renamed some of the variables to something more intuitive.

<img src="../screenshots/Pasted image 20220812184858.png" width=250>

`if (my_input_length == 0x1b)` reveals that the flag length is 27. And a look further down shows that each character of our possible flag is bitshifted by 2 before compared to our input:

<img src="../screenshots/Pasted image 20220812185233.png" width=500>

So I copied the values in an array and let python do the rest:

```
>>> flag = [0x1cc,0x1a0,0x194,0x1b0,0x1b0,0x18c,0x1d0,0x198,0x1ec,0x188,0xc4,0x1d0,0x15c,0x1a4,0xd4,0x194,0x17c,0xc0,0x1c0,0xcc,0x1c8,0x104,0x1d0,0xc0,0x1c8,0x14c,500]
>>> final_flag = ""
>>> for hex_num in flag:
...     final_flag += chr(hex_num >> 2)
... 
>>> final_flag
'shellctf{b1tWi5e_0p3rAt0rS}'
```
