# Keygen

Category: Reversing

> Enter the license key and get the flag.Simple right ? Flag Format:SHELLCTF{}.

---

We got an executable asking for a license key.

<img src="../screenshots/Pasted image 20220812214505.png" width=500>

As `strings` did not come up with something interesting, I opened the file in **Ghidra** and had a look at the main function.

<img src="../screenshots/Pasted image 20220812215030.png" width=500>

There in the while loop the entered key is processed and after that it's compared to `0x312`. I could have used that to actually find a valid key but at first I had a look at the `getString()` function.

<img src="../screenshots/Pasted image 20220812215145.png" width=500>

And there it was, the flag, character by character in hex. At that moment I felt like it would be faster to just type down these, than to write a keygen script.
