# Pulling The Strings

Category: Reversing

> Can you please feed me something? Flag Format: SHELLCTF{}

---

<img src="../screenshots/Pasted image 20220812174650.png" width=500>

We got an executable which wanted to be fed with something. The title of this challenge misled me, as I thought I will just have to pull `strings` but that did not come up with anything interesting. So I tried to have a look at it's behaviour in `radare2` This is what the disasseambled main function looked like:

<img src="../screenshots/Pasted image 20220812180120.png" width=500>

At **(1)** it asks us for food. At **(2)** (actually a bit below) it reads our input and at **(3)** it moves the flag into a register to compare it to our input. So flag would have to be there readable in the memory. I set a breakpoint after the `call sym.imp.fgetws` and another before the `call sym.imp.wcscmp` and continued to the first breakpoint.

<img src="../screenshots/Pasted image 20220812181517.png" width=250>

I fed it with a bunch of A's and had a look at the register memory.

<img src="../screenshots/Pasted image 20220812181552.png" width=500>

There were the eight A's from my input. So I continued to the next breakpoint and had another look at the register memory.

<img src="../screenshots/Pasted image 20220812181630.png" width=500>

And there it was, the flag, almost perfectly readable.
