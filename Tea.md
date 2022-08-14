### Tea
Reversing
> It's tea time. The flag format is shellctf{...}

![[Pasted image 20220812190850.png]]


Ghidra

![[Pasted image 20220812191630.png]]

flag length is 32 (0x20)

![[Pasted image 20220812191715.png]]

our input is in `pwd` variable

![[Pasted image 20220812192425.png]]

After adding Sugar, Tea and Milk, our input should look like: 
```
R;crc75ihl`cNYe`]m%50gYhugow~34i
```
So we need to reverse the process from this point. Need to remove milk, remove tea and remove sugar.

```

Description
The C library function char *strncat(char *dest, const char *src, size_t n) appends the string pointed to by src to the end of the string pointed to by dest up to n characters long.
```