# Secret Document

Category: Forensics

> "shell is the key if you did'nt get it xorry"

---

We got a file `Secret-Document.dat` which was not really readable.

<img src="../screenshots/Pasted image 20220812153524.png" width=500>

After ome brainstorming I just realized what the hint in the challenge description meant. I needed to xor the file with the key "shell". I came across this cool tool: https://github.com/hellman/xortool and used it to retrieve the original file which appeared to be a png image containing the flag.

<img src="../screenshots/Pasted image 20220812154739.png" width=500>

<img src="../screenshots/Pasted image 20220812154822.png" width=500>
