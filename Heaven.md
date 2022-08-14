### Heaven
Forensics
> "I was in the seventh heaven painted red green and blue"
> Flag Format: SHELL{s0mething_here}

![[Pasted image 20220812155348.png]]

played around in Gimp with Colour curves ... nothing

![[Pasted image 20220812155546.png]]

interesting: extension is `jpeg` but file type is `png`

![[Pasted image 20220812160139.png]]

![[Pasted image 20220812160241.png]]

https://unix.stackexchange.com/questions/22834/how-to-uncompress-zlib-data-in-unix

![[Pasted image 20220812162018.png]]


https://29a.ch/photo-forensics/
https://fotoforensics.com

![[Pasted image 20220812223024.png]]


![[Pasted image 20220812224617.png]]

zoomed in ... Hint says "painted red, green and blue"


https://trailofbits.github.io/ctf/forensics/

a lot of googling about png steganography

Google Reverse Image Search
--> stock image
![[Pasted image 20220813142923.png]]

tried to find difference with image magick

got a hint from some user to use **stegsolve**
https://github.com/zardus/ctf-tools/blob/master/stegsolve/install

![[Pasted image 20220813170334.png]]

SHELL{ma n1pul4t1ng_w1th_ 31ts_15_3A5y}