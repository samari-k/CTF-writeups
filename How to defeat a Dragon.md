### How to Defeat a Dragon
Reversing
> Dragonairre,the dragon with the hexadecimal head has attacked the village to take revenge on his last defeat,we need to get the ultimate weapon. Flag Format : SHELLCTF{}.

![[Pasted image 20220812215620.png]]

`strings` shows something interesting
![[Pasted image 20220812215828.png]]


Ghidra
![[Pasted image 20220812220513.png]]

SHELLCTF{5348454c4c4354467b31355f523376337235316e675f333473793f7d} 

```
┌──(kali㉿kali)-[~/shellctf/rev-dragon]
└─$ echo 5348454c4c4354467b31355f523376337235316e675f333473793f7d | xxd -r -p
SHELLCTF{15_R3v3r51ng_34sy?} 
```