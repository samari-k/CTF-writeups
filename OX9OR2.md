### OX9OR2
Crypto

Got encrypted message und the encryption function.

![[Pasted image 20220813210620.png]]

![[Pasted image 20220813210658.png]]

![[Pasted image 20220813211112.png]]

So this script generates the encryted message file out of a key file and a message file.
Here we can see that the key needs to have a length of 9 and is alphanumeric and that "SHELL" is part of the message.

As xor is reversible, it's easy to write a decryption script on base of the encryption script. I actually just changed some variable names.

![[Pasted image 20220813211212.png]]

But now I still need the key. As we know the flag starts either with `SHELL{` or `SHELLCTF{` and the latter has a length of nine, I decided to use that information to get the key.

![[Pasted image 20220813211526.png]]

![[Pasted image 20220813211545.png]]

Key looks strange but let's give it a try.

![[Pasted image 20220813211619.png]]

Nope. Close, but not yet there. So I had to just get a first part of the key and guess the other part.

![[Pasted image 20220813211737.png]]

![[Pasted image 20220813211829.png]]

That looked good enough.