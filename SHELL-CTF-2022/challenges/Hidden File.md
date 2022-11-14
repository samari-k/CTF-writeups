# Hidden File

Category: Forensics

> Our Agent gave us this image can you find whats there with this image?

---

We got an image file looking like this:

<img src="../screenshots/Pasted image 20220813124047.png" width=500>

<img src="../screenshots/Pasted image 20220813123834.png" width=500>

Interesting: manufacturer info says `the password is shell`. When there is a password, there is certainly some file inside the image, so I tried `steghide` and immediately got a secret zip file. Obviously I entered `shell` as passphrase.

<img src="../screenshots/Pasted image 20220813124554.png" width=500>

<img src="../screenshots/Pasted image 20220813124640.png" width=500>

At first I had a look at the PDF, which was just a kind of rickroll.

<img src="../screenshots/Pasted image 20220813124717.png" width=500>

Then I had a look at the JPG wich was a QR code leading to a youtube video. Got rickrolled again. So I focused on the `flag.zip` which also was password protected. Unfortunately the earlier obtained password did not work.

<img src="../screenshots/Pasted image 20220813124921.png" width=500>

<img src="../screenshots/Pasted image 20220813124947.png" width=500>

I defenitely needed another password, so I checked `something.jpg` again for information but found nothing hidden inside that. Then I checked again the pdf and there I found another password written very small in white colour on white background.

<img src="../screenshots/Pasted image 20220813130109.png" width=500>

This worked to extract flag.txt and get the flag.


