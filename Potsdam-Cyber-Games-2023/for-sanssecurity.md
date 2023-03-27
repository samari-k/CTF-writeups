# Park Sanssecurity

> Oh no! Someone stole HackHighInstitute's mascot (Modi the little Modem). 😟 Someone told you that the thief ran through Park Sanssecurity which is located next to the institute. There is also a security camera that could have captured the thief. Can you gain access to the image the camera took?


Ich mag das Wortspiel Im Titel dieser Challenge. Wir kriegen eine JPG Datei, ein Foto vom Potsdamer Schloss Sanssouci. Das Foto schein erstmal unauffällig.

![](screenshots/Pasted%20image%2020230317085731.png)

Die mit dem `exiftool` ausgelesenen Exif-Daten verbergen auch nichts auffälliges. Aber vielleicht ist ja was in der Datei selbst versteckt. Da hilft `binwalk`. Und tatsächlich scheint sich ein Zip-Archiv in dem Bild zu verstecken.

![](screenshots/Pasted%20image%2020230317085933.png)

Mit `-e` lässt es sich extrahieren. Es enthält offensicht eine Datei namens `thief.png` - die sich ohne Passwort allerdings nicht extrahieren lässt. Vielleicht ist das Passwort ja in irgendwelchen Kommentaren/Metadaten versteckt? Hier ist `strings` ein guter Helfer:

![](screenshots/Pasted%20image%2020230317090323.png)

Wenn das Archiv entpackt ist, zeigt `thif.png` die Flag und ein Foto vom Dieb. (Spoiler: Der Dieb ist Pikachu! 🙀)