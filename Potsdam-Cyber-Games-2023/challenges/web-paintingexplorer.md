# Painting Explorer

> Here you will find the Painting Explorer for our University, but the free version limits the number of shown paintings. To prevent DoS attacks, the site is rate limited.


Die Seite zeigt ein paar Bilder als Slideshow an und bietet eine Suche. Die Suche scheint allerdings nichts zurückzugeben, egal welchen Suchbegriff ich eingebe.

![](screenshots/Pasted%20image%2020230317094816.png)

Alsio habe ich mir die Requests in der BurpSuite angeschaut.  

![](screenshots/Pasted%20image%2020230317094933.png)

Anscheinend gehen die Suchanfragen an den Api-Endpunkt `/api/v1/paintings/?search=`.
Wenn der Suchbegriff genau so in eine SQL-Abfrage übernommen wird, könnte man es mit einer SQL-Injection versuchen, um sich alle Bilder-Daten anzeigen zu lassen. `'or 1;--` wäre zum Beuspiel ein guter erster Test-Kandidat. Und voilá:

![](screenshots/Pasted%20image%2020230317095614.png)

Die Flag befindet sich in einer der Bild-Informationen.